# JavaScript Document Object Model(DOM)

### What is the DOM?

The backbone of an HTML document are tags.

According to Document Object Model (DOM), every HTML-tag is an object. Nested tags are called “children” of the enclosing one.

All these objects are accessible using JavaScript.

[JavaScript.info - DOM Tree](https://javascript.info/dom-nodes)

### DOM Structure - Tree

The DOM is organized as a tree. A tree has a branching structure, has no cycles (a node may not contain itself, directly or indirectly), and has a single, well-defined root. In the case of the DOM, `document` serves as the root.

A way to visualize our document tree is as follows:
![DOM Tree Example](https://eloquentjavascript.net/img/html-tree.svg)
The leaves are text nodes, and the arrows indicate parent-child relationships between nodes.

[EloquentJavaScript.net - Chapter 14 - The Document Object Model](https://eloquentjavascript.net/14_dom.html)

### Moving through the DOM

DOM nodes contain a wealth of links to other nearby nodes. The following diagram illustrates these:
![DOM Tree Example](https://eloquentjavascript.net/img/html-links.svg)

- childNodes - Returns all children nodes of a node in an array like list ([NodeList](https://developer.mozilla.org/en-US/docs/Web/API/NodeList))
- firstChild & lastChild - Returns first or last child of a node
- nextSibling & previousSibling - Returns adjacent nodes, which are nodes with the same parent that appear immediately before or after the node itself

### Finding Elements

There are multiple methods available to find certain elements by tag name, class name or id:

- document.getElementById("firstTitle") - Finds the element with the id "firstTitle" (i.e. `<h1 id="firstTitle">Hello World!</h1>`)
- document.getElementByTagName("p") - Finds all paragraph elements with the tag `<p>some random paragraph text</p>`
- document.getElementByClassName(".sub-title") - Finds all elements with class "sub-title") (i.e. `<h3 class="sub-title">Some Sub Heading</h3>`) and returns an array like HTMLCollection.
- document.querySelector("h5.small-title") - Finds the first element which matches the CSS selector string (i.e `<h5 class="small-title">Small Heading</h5>`).
- document.querySelectorAll("h5.small-title") - Finds the all elements which matches the CSS selector string (i.e `<h5 class="small-title">Small Heading</h5>`) and returns them as an array like NodeList.

### Updating Elements

### Creating Elements

### More Resources

### Exercises

Take a look at the index.html file in this repository. Open the file in the Chrome web browser. You should see a checkout page created with the Bootstrap CSS framework.

Let's manipulate this example web page by using JavaScript.

1.
