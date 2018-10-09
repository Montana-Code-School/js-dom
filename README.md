# JavaScript Document Object Model(DOM)

### What is the DOM?

The backbone of an HTML document are tags.

According to Document Object Model (DOM), every HTML-tag is an object. Nested tags are called “children” of the enclosing one.

All these objects are accessible using JavaScript.

[JavaScript.info - DOM Tree](https://javascript.info/dom-nodes)

### DOM Structure - Tree

The DOM is organized as a tree. A tree has a branching structure, has no cycles (a node may not contain itself, directly or indirectly), and has a single, well-defined root. In the case of the DOM, `document` serves as the root.

A way to visualize our document tree is as follows: ![DOM Tree Example](https://eloquentjavascript.net/img/html-tree.svg)
The leaves are text nodes, and the arrows indicate parent-child relationships between nodes.

### Moving through the DOM

DOM nodes contain a wealth of links to other nearby nodes. The following diagram illustrates these: ![DOM Tree Example](https://eloquentjavascript.net/img/html-links.svg)

- childNodes - Returns all children nodes of a node in an array like list ([NodeList](https://developer.mozilla.org/en-US/docs/Web/API/NodeList))
- firstChild & lastChild - Returns first or last child of a node
- nextSibling & previousSibling - Returns adjacent nodes, which are nodes with the same parent that appear immediately before or after the node itself

### Finding Elements

There are multiple methods available to find certain elements by tag name, class name or id:

- [document.getElementById()](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById) - Finds the element with by the id (i.e. `<h1 id="firstTitle">Hello World!</h1>`)
- [document.getElementByTagName()](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementsByTagName) - Finds all elements with the specified tag (i.e. `<p>some random paragraph text</p>`)
- [document.getElementByClassName()](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementsByClassName) - Finds all elements with a certain class (i.e. `<h3 class="sub-title">Some Sub Heading</h3>`) and returns an array like HTMLCollection.
- [document.querySelector()](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector) - Finds the first element which matches the CSS selector string.
- [document.querySelectorAll()](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelectorAll) - Finds all elements which matches the CSS selector string and returns them as an array like NodeList.

### Changing the Document

Almost everything about the DOM data structure can be changed. The shape of the document tree can be modified by changing parent-child relationships. Nodes can be removed and additional nodes can be created and added to the document:

- [.remove()](https://developer.mozilla.org/en-US/docs/Web/API/ChildNode/remove) - Removes element
- [.createElement()](https://developer.mozilla.org/en-US/docs/Web/API/Document/createElement) - Creates a new element
- [.appendChild()](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild) - Appends new child element to parent element
- [.insertBefore()](https://developer.mozilla.org/en-US/docs/Web/API/Node/insertBefore) - Inserts the element as a child, right before an existing child, which is specified as a second argument.
- [innerHTML](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML) - Gets or sets (overwrites) all HTML wrapped by element

### Attributes & Styling

Some element attributes, such as [href](https://developer.mozilla.org/en-US/docs/Web/API/HTMLHyperlinkElementUtils/href) for links, can be accessed through a property of the same name on the element’s DOM object.

The styling of an element can be updated through the [element’s style property](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style). This property holds an object that has properties for all possible style properties. The values of these properties are strings, which we can write to in order to change a particular aspect of the element’s style.

### More Resources

- [EloquentJavaScript.net - Chapter 14 - The Document Object Model](https://eloquentjavascript.net/14_dom.html)
- [w3schools.com - JavaScript HTML DOM](https://www.w3schools.com/js/js_htmldom.asp)
- [Video - JavaScript DOM Tutorial by The Net Ninja](https://youtu.be/FIORjGvT0kk)
- [MDN - Node](https://developer.mozilla.org/en-US/docs/Web/API/Node)
- [MDN - Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)

### Exercises

Take a look at the index.html file in this repository. Open the file in the Chrome web browser. You should see a pricing page created with the Bootstrap CSS framework.

Let's manipulate this example web page by using JavaScript.

1. Remove the list item "Random Feature" under "Features in the footer
2. Add a link under "Resources" in the footer called "Super Resource"
3. Add a link under "About" called "Careers" between "Team" and "Locations"
4. Capitalize all letters in the "Sign Up" button in the header
5. Add the class "btn-outline-success" to the button "Sign Up for free" button in the "Free" card
6. Change the background color of all cards to "#f2fcfd"
7. Left align the pricing header by removing the class "text-center"
8. Change header in first pricing card from "Free" to "Non-Profit" and add a [Bootstrap Badge](https://getbootstrap.com/docs/4.1/components/badge/) called "Free" to the right of it.
