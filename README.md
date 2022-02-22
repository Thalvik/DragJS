# DragJS - An JavaScript library for Drag/Drop/Switch/Locked items ordering

DragJS in minimalistic JavaScript library for allowing HTML elements to be dragged and switched 
between each other. Why it does not utilize the replacement of source and target elements themselves,
it replaces their inner html and only on elements you specify it.

It also allows you to lock elements that should not be moved, and have an option to forbid replacement
of elements that do not have same class.

## Installing

Just include it as library

```javascript
<script src="index.js"></script>
```

## Usage
Call class DragJS
```javascript
new DragJS({
    elementsToSwitch : []
});
```

## Options

### elementsToSwitch
```javascript
    elementsToSwitch : []
```
This is the only required parameter for switching to actually have any UI effect. It allows you to define
which elements (as HTML tag) inside item container will be replaced from source to target ones and vice-versa. As
said, the library is not relying on replacing the whole item, just it's child elements.

Without this parameter only data-id will be switched between elements. Default ```[]```

### dragItemClass
```javascript
    dragItemClass : 'item'
```
Specify the class of item that will be checked in parent container of items. Default ```'item'```

### draggableClass
```javascript
    draggableClass : 'draggable'
```
Specify the class that item will have if it's set to be draggable with other ones. Default ```'draggable'```

### lockedClass
```javascript
    lockedClass : 'locked'
```
Specify the class that item will have if it's locked for dragging. Default ```'locked'```

### overClass
```javascript
    overClass : 'over'
```
Specify the class that item will have on drag start. Default ```'over'```

### inputOrder
```javascript
    inputOrder : 'drop-article-order'
```
Specify the id of input hidden element which value will be updated as JSON object of items as id and locked status. 
Default ```'drop-article-order'```

### lockedCheckboxSelector
```javascript
    lockedCheckboxSelector : 'lock-element'
```
Specify the class that checkbox element will have in order to lock parent item of it.
Default ```'lock-element'```

### checkSameClasses
```javascript
    checkSameClasses : []
```
Specify classes as strings, for which the library will check if both source and target item contains. If so,
the drag and drop will be allowed only between those items. For example, ```['orange', 'blue', 'yellow']```
you will put those as single class in each element.
Default ```[]```

## Example
Check following GitHub page for example usage: https://thalvik.github.io/index.html

## TODO
- Add linter
- Add unit testing
- Publish on npm