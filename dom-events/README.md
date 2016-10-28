## Focus Events

|Event Name|Description|Bubbles|Browser|
|----------|----------|-------|--------|
|[focus](https://developer.mozilla.org/en-US/docs/Web/Events/focus)  |Element has received focus|No|All|
|[focusin](https://developer.mozilla.org/en-US/docs/Web/Events/focusin)  |Element has received focus|Yes|[All Except FF](http://caniuse.com/#feat=focusin-focusout-events)|
|[blur](https://developer.mozilla.org/en-US/docs/Web/Events/blur)  |Element has lost focus|No|All|
|[focusout](https://developer.mozilla.org/en-US/docs/Web/Events/focusout)  |Element has lost focus|Yes|[All Except FF](http://caniuse.com/#feat=focusin-focusout-events)|


## Mouse Events

|Event Name|Description|Bubbles|Browser|Default Action|
|----------|-----------|-------|-------|--------------|
|[mouseenter](https://developer.mozilla.org/en-US/docs/Web/Events/mouseenter) |pointer/mouse is moved onto the element|No|All|None|
|[mouseover](https://developer.mozilla.org/en-US/docs/Web/Events/mouseover) |pointer/mouse is moved onto the element or its children|Yes|All|None|
|[mouseleave](https://developer.mozilla.org/en-US/docs/Web/Events/mouseleave) |pointer/mouse is moved off the element|No|All|None|
|[mouseout](https://developer.mozilla.org/en-US/docs/Web/Events/mouseout) |pointer/mouse is moved off the element or its children|Yes|All|None|
|[mousemove](https://developer.mozilla.org/en-US/docs/Web/Events/mousemove) |pointer/mouse is moved while over an element.|Yes|All|None|
|[mousedown](https://developer.mozilla.org/en-US/docs/Web/Events/mousedown) |pointer/mouse button is pressed on an element.|Yes|All|Varies - select, scroll etc|
|[mouseup](https://developer.mozilla.org/en-US/docs/Web/Events/mouseup) |pointer/mouse button is released over an element|Yes|All|Context menu, if right button is pressed|
|[click](https://developer.mozilla.org/en-US/docs/Web/Events/click) |pointer/mouse button has been pressed and released on an element.|Yes|All|Varies - select, action etc|
|[dblclick](https://developer.mozilla.org/en-US/docs/Web/Events/dblclick) |pointer/mouse button is clicked twice on an element|Yes|All|Varies - Text Select etc|


#### Mouse event object

|Attribute|Description|Values      |Browser|
|----------|-----------|-----------|-------|
|[altKey](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/altKey) |Returns true if the alt key was down when the mouse event was fired|true/false|All|
|[ctrlKey](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/ctrlKey) |Returns true if the ctrl key was down when the mouse event was fired|true/false|All|
|[metaKey](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/metaKey) |Returns true if the meta/command/windows key was down when the mouse event was fired|true/false|All|
|[clientX/Y](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/clientX) | X/Y coordinate of the mouse pointer in local (DOM content) coordinates|pixels|All|
|[pageX/Y](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/pageX) | returns the horizontal/vertical coordinate of the event relative to the whole document|pixels|IE9+|
|[screenX/Y](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/screenX) |  X/Y coordinate of the mouse pointer in global (screen) coordinates|pixels|All|
|[movementX/Y](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/movementX) |  X/Y coordinate of the mouse pointer relative to the position of the last mousemove event|pixels|No IE/Safari|
|[offsetX/Y](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/offsetX) | X/Y Offset of the mouse pointer between that event and the padding edge of the target node|pixels|All|
|[button](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/button) |Indicates which button was pressed on the mouse to trigger the event|<ul><li>0 - Main</li><li>1 - Auxiliary</li><li>2 - Secondary</li></ul>|IE9+|
|[buttons](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/buttons) |Indicates which buttons are pressed on the mouse when the event is triggered, the values are combined if more than button is pressed| <ul><li>0 - None</li><li>1 - Left</li><li>2 - Right</li><li>4 - Middle</li></ul> |IE9+, No Safari|
|[which](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/buttons) |Indicates which buttons are pressed on the mouse when the event is triggered, the values are combined if more than button is pressed| <ul><li>0 - None</li><li>1 - Left</li><li>2 - Right</li><li>4 - Middle</li></ul> |IE9+|

## Keyboard Events

## Touch Events

## Form Events

