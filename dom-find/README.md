## General Querying
Methods to query element/document based provided criteria

| Method | Applied on  | Argument | Returns | Description   |Browser    |
|------------|-------------|------------|-----------|------------|-----------|
|[getElementById](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById) | document | id of element| Element| Searches and returns an element with the given id|All|
|[getElementsByClassName](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementsByClassName) | document/element | Class name string | Live Node List | Returns all child elements having the given class|IE9+|
|[getElementsByTagName](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementsByTagName) | document/element | Tag name string | Live Node List | Returns all child elements with the given tag|All|
|[getElementsByName](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementsByName) | document | Element name string | Live Node List | Returns all child elements having given name attribute|IE9+*[1]|
|[querySelector](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector) | document/element | One or more CSS selectors string separated by commas | Element | Returns the first child element matching the given selector(s)|All|
|[querySelectorAll](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelectorAll) | document/element | One or more CSS selectors string separated by commas | Node List | Returns list of child elements matching the given selector(s)|All|

[1] In IE/Opera getElementsByName() method will also return elements that have an id attribute with the specified value

## DOM Tree Querying

Properties to find elements based on DOM tree:-

| Node property   | Element property  | Returns      | Description |Browser     |
|-----------------|-------------------|--------------|-------------|------------|
|[childNodes](https://developer.mozilla.org/en-US/docs/Web/API/Node/childNodes) | [children](https://developer.mozilla.org/en-US/docs/Web/API/ParentNode/children) | Live Node List | Returns all child nodes/elements of the Node|All/IE9+|
|[parentNode](https://developer.mozilla.org/en-US/docs/Web/API/Node/parentNode) | [parentElement](https://developer.mozilla.org/en/docs/Web/API/Node/parentElement) | Node/Element | Returns the parent node/element of the specified node|All/IE9+|
|[firstChild](https://developer.mozilla.org/en-US/docs/Web/API/Node/firstChild) | [firstElementChild](https://developer.mozilla.org/en-US/docs/Web/API/ParentNode/firstElementChild) | Node/Element | Returns the node's first child node/element in the tree, or null |All/IE9+|
|[lastChild](https://developer.mozilla.org/en-US/docs/Web/API/Node/lastChild) | [lastElementChild](https://developer.mozilla.org/en-US/docs/Web/API/ParentNode/lastElementChild) | Node/Element | Returns the last child node/element of the specified node|All/IE9+|
|[nextSibling](https://developer.mozilla.org/en-US/docs/Web/API/Node/nextSibling) | [nextElementSibling](https://developer.mozilla.org/en-US/docs/Web/API/NonDocumentTypeChildNode/nextElementSibling) | Node/Element | Returns the node/element immediately following the specified node at the same level|All/IE9+|
|[previousSibling](https://developer.mozilla.org/en-US/docs/Web/API/Node/previousSibling) | [previousElementSibling](https://developer.mozilla.org/en-US/docs/Web/API/NonDocumentTypeChildNode/previousElementSibling) | Node/Element | Returns the node/element preceding the specified node at the same level|All/IE9+|

* In IE/Opera parentElement is only present on element nodes
* Node properties return any DOM node like element, comment, cddata etc, while element properties only returns element nodes

## Tree Walker Querying
* Querying using the [Tree Walker API](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker)
* It is created using document.createTreeWalker(root, nodesToShow, filter, entityExpandBol)
  * root: The root node to begin searching the document tree using
  * nodesToShow: The type of nodes that should be visited by TreeWalker
  * filter (or null): Reference to custom function (NodeFilter object) to filter the nodes returned
  * entityExpandBol: Boolean parameter specifying whether entity references should be expanded.
* The below no-argument methods can be applied to the TreeWalker object:-

| Methods    | Description   |Browser |
|------------|-----------|------------|
|[firstChild()](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker/firstChild)|Travels to and returns the first child of the current node|IE9+|
|[lastChild()](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker/lastChild)|Travels to and returns the last child of the current node|IE9+|
|[parentNode()](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker/parentNode)|Travels to and returns the current node's parent node|IE9+|
|[nextNode()](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker/nextNode)|Travels to and returns the next node within the filtered collection of nodes|IE9+|
|[nextSibling()](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker/nextSibling)|Travels to and returns the next sibling of the current node|IE9+|
|[previousNode()](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker/previousNode)|Travels to and returns the previous node of the current node|IE9+|
|[previousSibling()](https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker/previousSibling)|Travels to and returns the previous sibling of the current node|IE9+|

#### Notes
* In general this is slower the General and DOM Tree Querying methods

## Node Iterator Querying
* [NodeIterator](https://developer.mozilla.org/en/docs/Web/API/NodeIterator) represents an iterator over the members of a list of the nodes in a subtree of the DOM.
* A NodeIterator can be created using the document.createNodeIterator(root, nodesToShow, filter)
  * root: The root node to begin searching the document tree using
  * nodesToShow: The [type of nodes](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator/whatToShow) that should be iterated
  * filter (or null): Reference to custom function ([NodeFilter](https://developer.mozilla.org/en-US/docs/Web/API/NodeFilter) object) to filter the nodes returned
* It supports the below methods for iteration

| Methods    | Description   |Browser |
|------------|---------------|------------|
|[previousNode()](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator/nextNode)|Returns the previous Node in the document, or null if there are none|IE9+|
|[nextNode()](https://developer.mozilla.org/en-US/docs/Web/API/NodeIterator/previousNode)|Returns the next Node in the document, or null if there are none|IE9+|
