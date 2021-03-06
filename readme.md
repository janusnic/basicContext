# basicContext

Easy-to-use context-menu for your website or webapp.

![Context Screenshot](http://l.electerious.com/uploads/big/9f182a325203b158e59ad48aaebb13a2.png)

## Demos

| Name | Description | Link |
|:-----------|:------------|:------------|
| Basic demo | basicContext works with all kind of events | [Try it on CodePen](http://codepen.io/electerious/pen/emaJxE) |
| Position demo | basicContext never leaves the visible screen-area | [Try it on CodePen](http://codepen.io/electerious/pen/GJqrZN) |
| Scroll demo | basicContext is scrollable when the context height is bigger than the browser height | [Try it on CodePen](http://codepen.io/electerious/pen/aOZpZr) |

## Features

- Works in all modern browsers
- Written in Vanilla JS
- Stays within the viewport and never opens outside the visible screen-area ([Demo](http://codepen.io/electerious/pen/GJqrZN))
- Scrollable, when the height of the context-menu is bigger than the height of the browser ([Demo](http://codepen.io/electerious/pen/aOZpZr))

## Requirements

basicContext is written in Vanilla JS and only dependents on the following browser APIs:

- [classList](http://caniuse.com/#feat=classlist)

All of these APIs are capable of being polyfilled in older browser. Check the linked resources above to determine if you must polyfill to achieve your desired level of browser support.

## Installation

	bower install basicContext
	
## How to use

Simply include the following files in your HTML:

```html
<link type="text/css" rel="stylesheet" href="bower_components/basicContext/dist/basicContext.min.css">
<script async type="text/javascript" src="bower_components/basicContext/dist/basicContext.min.js"></script>
```

Show a context-menu by using the following command:

```js
var items = [
	{ type: 'item', title: 'Add Sites', icon: 'ion-plus-round', fn: function() {} },
	{ type: 'item', title: 'Reset Login', icon: 'ion-person', fn: function() {} },
	{ type: 'item', title: 'Help', icon: 'ion-help-buoy', fn: function() {} },
	{ type: 'separator' },
	{ type: 'item', title: 'Logout', icon: 'ion-log-out', fn: function() {} }
]

basicContext.show(items, e)
```