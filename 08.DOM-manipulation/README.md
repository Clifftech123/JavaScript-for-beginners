# Javascript DOM Manipulation

**What is DOM Manipulation?**
The DOM in dom manipulation in javascript stands for Document Object Model. The Document Object Model (DOM) is a tree-like structure illustrating the hierarchical relationship between various HTML elements.In the DOM, every element, attribute, and piece of text in an HTML or XML document is represented as a node. Each node is an object with properties and methods that allow it to be manipulated and interacted with using JavaScript.

A visual representation of the DOM tree is shown in the image below.
![dom](/images/1-1.jpg)

- **Document** is the core/foundation of the DOM.
- **HTML** Root element is the child of the document object.
- **Body** and **Head** are the children of the HTML element and siblings to each other.
- **Title** Element is the parent to the text node: "my text” and the child of the head element.
- **a** and **h1** tag are the children of the body element and siblings to each other.
- **herf** attribute is the children of the a(anchor) tag.

The DOM is referred to as a programming API for XML and HTML documents. DOM defines the logical structure of documents and the methods for accessing and changing them are specified by the DOM.

### How to Select Elements in the DOM?

n JavaScript, you can select elements in the DOM (Document Object Model) using various methods. Here are some commonly used methods for selecting elements in the DOM .There are several ways to select elements in the DOM. The most common ways are:

- **document.getElementById()**: This method selects an element by its id attribute.
- Example:

  ```javascript
  const element = document.getElementById("myId");
  ```

- **document.getElementsByClassName()**: This method selects elements by their class attribute.

Example:

```javascript
const elements = document.getElementsByClassName("myClass");
```

- **document.getElementsByTagName()**: This method selects elements by their tag name.

  Example:

  ```javascript
  const elements = document.getElementsByTagName("p");
  ```

- **document.querySelector()**: This method selects the first element that matches a specified CSS selector(s).

  Example:

  ```javascript
  const element = document.querySelector("p");
  ```

- **document.querySelectorAll()**: This method selects all elements that match a specified CSS selector(s).

  Example:

  ```javascript
  const elements = document.querySelectorAll("p");
  ```

The querySelector() and querySelectorAll() methods are especially useful because they allow you to select elements using CSS selectors, which gives you a lot of flexibility in terms of selecting specific elements or groups of elements based on their attributes, classes, or structure.

- **ParentNode :** This property returns the parent node of an element.

  Example:

  ```javascript
  const myElement = document.getElementById("my-id");
  const parentElement = myElement.parentNode;
  ```

- **ChildNodes :** This property returns a collection of an element's child nodes, as a NodeList object.

  Example:

  ```javascript
  const myElement = document.getElementById("my-id");
  const childNodes = myElement.childNodes;
  ```

- **FirstChild** and **LastChild:** These properties return the first and last child nodes of an element.

```javascript
const myElement = document.getElementById("my-id");
const firstChild = myElement.firstChild;
const lastChild = myElement.lastChild;
```

- **PreviousSibling** and **NextSibling:** These properties return the previous and next sibling nodes of an element.

```javascript
const myElement = document.getElementById("my-id");
const nextSibling = myElement.nextSibling;
const previousSibling = myElement.previousSibling;
```

- **appendChild() :** This method adds a new child node to an element.

  ```js
  const myElement = document.getElementById("my-id");
  const newChild = document.createElement("div");
  myElement.appendChild(newChild);
  ```

- **removeChild() :** This method removes a child node from an element.

  ```js
  const myElement = document.getElementById("my-id");
  const childToRemove = myElement.firstChild;
  myElement.removeChild(childToRemove);
  ```

- **insertBefore() :** This method inserts a new node before an existing child node of an element.

  ```js
  const myElement = document.getElementById("my-id");
  const newChild = document.createElement("div");
  const referenceChild = myElement.firstChild;
  myElement.insertBefore(newChild, referenceChild);
  ```

- **replaceChild() :** This method replaces a child node of an element with a new node.

  ```js
  const myElement = document.getElementById("my-id");

  const newChild = document.createElement("div");

  const oldChild = myElement.firstChild;

  myElement.replaceChild(newChild, oldChild);
  ```

  By using these methods, you can traverse and manipulate the DOM tree in a flexible and powerful way. With some practice, you can use these methods to create dynamic and interactive web pages that respond to user input and provide a rich user experience.



