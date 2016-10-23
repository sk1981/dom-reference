
## Classes/Styles
| property| description| browser|
|---------|------------|--------|
|[Element.className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className)|className gets and sets the value of the class attribute of the specified element|All|
|[Element.style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style)|object that sets and gets the element's inline style attribute|All|

| method  | arguments  | description| browser|
|---------|------------|------------|--------|
|[Window.getComputedStyle](https://developer.mozilla.org/en-US/docs/Web/API/Window/getComputedStyle)|1. element 2. pseudo Element (optional)|Returns a read-only object which can be used to inspect the element's applied style|IE10+|

#### Element.classlist
Methods on [element.classList](https://developer.mozilla.org/en/docs/Web/API/Element/classList) can be used to add/update the classes

| method  | arguments  | description| browser|
|---------|------------|------------|--------|
|add|comma separate list of clases|classes provided are added if not already present|IE10+|
|remove|comma separate list of clases|Remove specified classes if already present|IE10+|
|toggle |className|toggles the provided className|IE10+|
|contains |className|Checks if specified class is present on the element |IE10+|
|item  | index as number| Return class value present at the given index|IE10+|

## Attribute

| property| description| browser|
|---------|------------|--------|
|Element.attributes|Returns a live collection of all attribute nodes registered to the specified node|All|

| method  | arguments  | description| browser|
|---------|------------|------------|--------|
|[Element.getAttribute](https://developer.mozilla.org/en-US/docs/Web/API/Element/getAttribute)|attributeName |Returns the value of a specified attribute on the element|All|
|[Element.setAttribute](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttribute)|attributeName, attributeValue |Adds a new attribute or changes the value of an existing attribute on the specified element. |All|
|[Element.removeAttribute](https://developer.mozilla.org/en-US/docs/Web/API/Element/removeAttribute)|attributeName |Removes the specified attribute from the given element.|All|
|[Element.hasAttribute](https://developer.mozilla.org/en-US/docs/Web/API/Element/hasAttribute)|attributeName |returns a Boolean indicating whether the element has the specified attribute or not.|All|

* There are alternative versions present for interacting with Nodes - getAttributeNode, setAttributeNode and removeAttributeNode which are not very used much

#### Dataset API

* The [HTMLElement.dataset](https://developer.mozilla.org/en/docs/Web/API/HTMLElement/dataset) property allows access, both in reading and writing mode, to all the custom data attributes (data-*) set on the element.

| property| description| browser|
|---------|------------|--------|
|Element.dataset| Map of DOMString, one entry for each custom data attribute|IE11+|
|Element.dataset.xYZ| Gets and sets the property 'data-z-y-z'|IE11+|


## Text

| property                 | description| browser|
|--------------------------|------------|--------|
|[Node.innerText](https://developer.mozilla.org/en-US/docs/Web/API/Node/innerText)| Nonstandard property that represents the text content of a node and its descendants as it appears on page|All, Moz 45+|
|[Node.outerText](https://developer.mozilla.org/en-US/docs/Web/API/Node/innerText)| Nonstandard property gets same value as innerText, when set it replaces the current node.|All except FF|
|[Node.textContent](https://developer.mozilla.org/en/docs/Web/API/Node/textContent)| Represents the text content of a node and its descendants|IE9+|

| method  | arguments  | description| browser|
|---------|------------|------------|--------|
|[Element.insertAdjacentText](https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentText)|1. position: 'beforebegin/afterbegin/beforeend/afterend', 2. text string |Method inserts the given text node at a given position relative to the element it is invoked upon|All|

## HTML

| property                 | description| browser|
|--------------------------|------------|--------|
|[Element.innerHTML](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML)| innerHTML sets or gets the serialized HTML fragment describing the element's descendants|All|
|[Element.outerHTML](https://developer.mozilla.org/en-US/docs/Web/API/Element/outerHTML)| outerHTML sets or gets the serialized HTML fragment describing the element including its descendants. |All|

| method  | arguments  | description| browser|
|---------|------------|------------|--------|
|[Element.insertAdjacentHTML](https://developer.mozilla.org/en/docs/Web/API/Element/insertAdjacentHTML)|1. position: 'beforebegin/afterbegin/beforeend/afterend', 2. HTML string |parses the specified text as HTML and inserts the resulting nodes into the DOM tree at a specified position|All|
