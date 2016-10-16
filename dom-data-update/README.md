## Classes
| property| description| browser|
|---------|------------|--------|
|Element.className|className gets and sets the value of the class attribute of the specified element|All|


#### Element.classlist
Methods on element.classList can be used to add/update the classes

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
|Element.getAttribute|attributeName |Returns the value of a specified attribute on the element|All|
|Element.setAttribute|attributeName, attributeValue |Adds a new attribute or changes the value of an existing attribute on the specified element. |All|
|Element.removeAttribute|attributeName |Removes the specified attribute from the given element.|All|
|Element.hasAttribute|attributeName |returns a Boolean indicating whether the element has the specified attribute or not.|All|

* There are alternative versions present getAttributeNode, setAttributeNode and removeAttributeNode which are not very used much
