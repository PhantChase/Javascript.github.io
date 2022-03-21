# PROJECT: A PLATFORM GAME

## The Game

Try the game on www.lessmilk.com/games/10

## The Technology

## Levels

## Reading a Level

## Actors

```
class Vec {
	constructor(x, y) {
		this.x = x; this.y = y;
	}
	plus(other) {
		return new Vec(this.x + other.x, this.y + other.y);
	} times(factor) {
		return new Vec(this.x * factor, this.y * factor);
	}
}
```

## Encapsulation as a Burden
## Drawing

```
function elt(name, attrs, ...children) {
	let dom = document.createElement(name);
	for (let attr of Object.keys(attrs)) {
		dom.setAttribute(attr, attrs[attr]);
	} for (let child of children) {
		dom.appendChild(child);
	}
	return dom;
}
```

```
class DOMDisplay {
	constructor(parent, level) {
		this.dom = elt("div", {class: "game"}, drawGrid(level));
		this.actorLayer = null;
		parent.appendChild(this.dom);
	}
	
	clear() { this.dom.remove(); }
}
```


## Motion and Collision

## Actor Updates

## Tracking Keys

## Running the Game
