##Bounding Box
* The [getBoundingClientRect()](https://developer.mozilla.org/en/docs/Web/API/Element/getBoundingClientRect) returns an object with the below fields:-

| Field | Description |Browser |
|-------|-------------|------------|
|bottom | vertical distance from ***bottom*** of box to viewport|All|
|top | vertical distance from ***top*** of box to viewport|All|
|left | horizontal distance from ***left*** of box to viewport|All|
|right | horizontal distance from ***left*** of box to viewport|All|
|height | ***height*** of the box (includes padding + border)|IE9+|
|width | ***width*** of the box (includes padding + border)|IE9+|

* Note that the distances are from viewport and not document
   * Hence scroll position needs to be take into account if distance from document is needed.

## Element Position
Properties to get the current element position

| X Position | Y Position  |Description |Browser    |
|------------|-------------|------------|-----------|
|BCR.left     | BCR.top     | distance from ***bottom*** of box to viewport|IE9+|
|[offsetLeft](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/offsetTop) | [offsetTop](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/offsetTop)  | distance from top-left of element to Offset Parent|All|
* BCR = getBoundingClientRect

## Scroll Position
Properties to get the current scroll values

| X Position | Y Position  |Description |Applied    |ReadOnly   |Browser    |
|------------|-------------|------------|-----------|-----------|-----------|
|[pageXOffset](https://developer.mozilla.org/en-US/docs/Web/API/Window/pageXOffset) | [pageYOffset](https://developer.mozilla.org/en-US/docs/Web/API/Window/pageYOffset) | Number of pixels that the document has scrolled left/top|window|Yes|IE9+|
|[scrollX](https://developer.mozilla.org/en-US/docs/Web/API/Window/scrollX) | [scrollY] (https://developer.mozilla.org/en-US/docs/Web/API/Window/scrollY) | Alias for pageXOffset/pageYOffset|window|Yes|No IE|
|[scrollLeft](https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollLeft)  | [scrollTop](https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollTop) | Gets or sets the number of pixels that an element's content is scrolled|Element|Yes|IE9+,*[1]|
* [1] WebKit/Blink, use scrollTop/Left on document.body instead of document.documentElement

## Mouse Position
* Properties to get the current position of mouse pointer.
* All these properties are are only present on mouse event object

| X Position | Y Position  |Description |Browser    | Reference Point |
|------------|-------------|------------|-----------|-----------------|
|[clientX](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/clientX) | [clientY](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/clientY)| Relative to the whole document. |All| Document Root|
|[screenX](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/screenX) | [screenY](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/screenY)| Relative to the top left of the physical screen/monitor|All| Physical Screen|
|[pageX](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/pageX) | [pageY](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/pageY) | Relative to the upper left edge of the content area (Viewport) |9+| Viewport/Viewable Content Area|

## Dimensions
| Height      | Width       |Description  |Applied    |ReadOnly   |Browser    |
|-------------|--------------|------------|-----------|-----------|-----------|
|[offsetHeight](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/offsetHeight) | [offsetWidth](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/offsetWidth) | Height/Width of the element including padding & borders|window|Yes|IE7+|
|[scrollHeight](https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollHeight) | [scrollWidth](https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollWidth) |  Height/Width of the element including padding & content not visible on the screen due to overflow|window|Yes|IE9+|
|[clientHeight](https://developer.mozilla.org/en-US/docs/Web/API/Element/clientHeight) | [clientWidth](https://developer.mozilla.org/en-US/docs/Web/API/Element/clientWidth) | Height/Width including just padding |window|Yes|IE9+|

####Notes
* if box-sizing = border-box, then css height === scrollHeight
* Bounding Box height/width are same as offsetHeight/Width
* element.scrollHeight - element.scrollTop === element.clientHeight
