# PART I
## ASYNCHRONOUS PROGRAMMING
### Asynchronicity
### Crow Tech
### Callbacks
```
import {defineRequestType} from "./crow-tech"

defineRequestType("note", (nest, content, source, done) => {
console.log(`${nest.name} received note: ${content}`); done(); });
```
### Promises
```
function storage(nest, name) {
	return new Promise(resolve => {
		nest.readStorage(name, result => resolve(result));
		});
}
storage(bigOak, "enemies")
	.then(value => console.log("Got", value));
```
### Failure
```
const {parse} = require("ini");
console.log(parse("x = 10\ny = 20"));
// → {x: "10", y: "20"}
```
### ECMAScript Modules
### Networks Are Hard
### Collections of Promises
```
requestType("ping", () => "pong");

function availableNeighbors(nest) {
	let requests = nest.neighbors.map(neighbor => {
	return request(nest, neighbor, "ping")
		.then(() => true, () => false);
	});
	return Promise.all(requests).then(result => {
		return nest.neighbors.filter((_, i) => result[i]);
	});
}
```
### Network Flooding
```
import {everywhere} from "./crow-tech";
everywhere(nest => {
	nest.state.gossip = [];
});

function sendGossip(nest, message, exceptFor = null) {
	nest.state.gossip.push(message);
	for (let neighbor of nest.neighbors) {
		if (neighbor == exceptFor) continue;
		request(nest, neighbor, "gossip", message);
	}
} 
requestType("gossip", (nest, message, source) => {
	if (nest.state.gossip.includes(message)) return;
	console.log(`${nest.name} received gossip '${
			message}' from ${source}`);
	sendGossip(nest, message, source);
});
```
### Message Routing
```
function routeRequest(nest, target, type, content) {
	if (nest.neighbors.includes(target)) {
		return request(nest, target, type, content);
	} else {
		let via = findRoute(nest.name, target, nest.state.connections);
	if (!via) throw new Error(`No route to ${target}`);
	return request(nest, via, "route", {target, type, content});
	}
} requestType("route", (nest, {target, type, content}) => { return routeRequest(nest, target, type, content); });
```