## Node Creation
Methods to create instances of DOM Element/Node.

| Method | Argument | Returns | Description   |Browser    |
|------------|-------------|------------|-----------|------------|-----------|
|[document.createElement](https://developer.mozilla.org/en-US/docs/Web/API/Document/createElement) |  tag name of the element| HTML Element|  Creates the HTML element specified by tagName|All|
|[document.createTextNode](https://developer.mozilla.org/en-US/docs/Web/API/Document/createTextNode) | text content string | Text node |  Creates a new Text node|All|
|[document.createAttribute](https://developer.mozilla.org/en-US/docs/Web/API/Document/createAttribute) | attribute name | Attribute node |  Creates a new attribute node|All|
|[document.createComment](https://developer.mozilla.org/en-US/docs/Web/API/Document/createComment) | comment string | Comment node |  Creates a new comment node|All|


## Node Insertion
Methods to insert the given node in the DOM

| Method | Argument | Returns | Description   |Browser    |
|------------|-------------|------------|-----------|------------|-----------|
|[node.insertBefore](https://developer.mozilla.org/en-US/docs/Web/API/Node/insertBefore) |  <ol><li>New node to be inserted</li><li>A reference node</li></ol>| HTML Element|  Inserts the specified new node before the reference node as a child of the current node.|All|
|[node.appendChild](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild) |  New node | Appended child node| Adds a node as the last child of the specified parent node|All|
|[element.insertAdjacentElement](https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentElement) | <ol><li>position: 'beforebegin/afterbegin/beforeend/afterend'</li><li>Element to be inserted</li></ol> | Element which was inserted| Inserts the element node at a given position relative to the element it is invoked upon|All|
|[element.insertAdjacentText](https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentText) | <ol><li>position: 'beforebegin/afterbegin/beforeend/afterend'</li><li> DOMString representing the text to be inserted </li></ol> | void| Inserts the text string as node at a given position relative to the element it is invoked upon|All|

