##Bounding Box
* The getBoundingClientRect() returns an object with the below fields:-

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
|BB.top      | BB.left     | distance from ***bottom*** of box to viewport|IE9+|
|offsetTop   | offsetLeft  | distance from top-left of element to Offset Parent|All|
* BBCR = getBoundingClientRect

## Scroll Position
Properties to get the current scroll values

| X Position | Y Position  |Description |Applied    |ReadOnly   |Browser    |
|------------|-------------|------------|-----------|-----------|-----------|
|pageXOffset | pageYOffset | Number of pixels that the document has scrolled left/top|window|Yes|IE9+|
|scrollX     | scrollY     | Alias for pageXOffset/pageYOffset|window|Yes|No IE|
|scrollLeft  | scrollTop   | Gets or sets the number of pixels that an element's content is scrolled|Element|Yes|IE9+,*[1]|
* [1] WebKit/Blink, use scrollTop/Left on document.body instead of document.documentElement

## Mouse Position
* Properties to get the current position of mouse pointer.
* All these properties are are only present on mouse event object

| X Position | Y Position  |Description |Browser    | Reference Point |
|------------|-------------|------------|-----------|-----------------|
|clientX     | clientY     | Relative to the whole document. |All| Document Root|
|screenX     | screenY     | Relative to the top left of the physical screen/monitor|All| Screen|
|pageX       | pageY       | Relative to the upper left edge of the content area (Viewport) |9+| Viewport|

## Dimensions
| Height      | Width       |Description  |Applied    |ReadOnly   |Browser    |
|-------------|--------------|------------|-----------|-----------|-----------|
|[offsetHeight](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/offsetHeight) | offsetWidth | Height/Width of the element including padding & borders|window|Yes|IE7+|
|[scrollHeight](https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollHeight) | scrollWidth |  Height/Width of the element including padding & content not visible on the screen due to overflow|window|Yes|IE9+|
|[clientHeight](https://developer.mozilla.org/en-US/docs/Web/API/Element/clientHeight) | clientWidth | Height/Width including just padding |window|Yes|IE9+|

####Notes
* if box-sizing = border-box, then css height === scrollHeight
* Bounding Box height/width are same as offsetHeight/Width
* element.scrollHeight - element.scrollTop === element.clientHeight


