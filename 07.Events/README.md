## JavaScript events

**Introduction:**
JavaScript events are actions or occurrences that happen in the browser, such as a user clicking a button or typing into a text field. Events can be triggered by the user or by the browser, and JavaScript provides a way to respond to these events.

**Types of JavaScript Events:**
There are many types of JavaScript events, but they can generally be categorized into three types: user events, browser events, and system events.

**_User events:_** are events that are initiated by the user, such as clicking a button, typing into a text field, or scrolling the page. These events are the most common type of events in JavaScript.

Here are some examples of user events in JavaScript:

- Click Event:
  The most common user event in JavaScript is the click event. This event is triggered when the user clicks on an element, such as a button or a link. Here is an example of how to handle a click event:

```javascript
const button = document.querySelector("button");

button.addEventListener("click", function () {
	console.log("Button clicked!");
});
```

In this example, an event listener is added to a button element. When the button is clicked, the function inside the event listener is executed and the message "Button clicked!" is logged to the console.

- Keydown Event:
  Another common user event is the keydown event. This event is triggered when the user presses a key on the keyboard. Here is an example of how to handle a keydown event:

```javascript
document.addEventListener("keydown", function (event) {
	console.log("Key pressed: " + event.key);
});
```

In this example, an event listener is added to the entire document. When the user presses a key, the function inside the event listener is executed and the message "Key pressed: [key]" is logged to the console, where [key] is replaced with the actual key that was pressed.

- Mousemove Event: Another common user event is the mousemove event. This event is triggered when the user moves the mouse. Here is an example of how to handle a mousemove event:

```javascript
const container = document.querySelector(".container");

container.addEventListener("mousemove", function (event) {
	console.log("Mouse position: " + event.clientX + ", " + event.clientY);
});
```

In this example, an event listener is added to a container element. When the user moves the mouse over the container, the function inside the event listener is executed and the message "Mouse position: [x], [y]" is logged to the console, where [x] and [y] are replaced with the x and y coordinates of the mouse cursor.

These are just a few examples of the many user events that can be handled in JavaScript. There are many more events that can be handled, such as the keyup event, the keypress event, the mousedown event, the mouseup event, the mouseover event, the mouseout event, the scroll event, the resize event, the focus event, the blur event, and many more.

**_Browser events:_** are events that are triggered by the browser, such as when a page is loaded or when an image is loaded.

Here are some examples of browser events in JavaScript:

- Load Event:
  The most common browser event in JavaScript is the load event. This event is triggered when the browser has finished loading the page. Here is an example of how to handle a load event:

```javascript
window.addEventListener("load", function () {
	console.log("Page loaded!");
});
```

In this example, an event listener is added to the window object. When the browser has finished loading the page, the function inside the event listener is executed and the message "Page loaded!" is logged to the console.

- Beforeunload Event:
  Another common browser event is the beforeunload event. This event is triggered when the user is about to leave the page. Here is an example of how to handle a beforeunload event:

```javascript
window.addEventListener("beforeunload", function (event) {
	event.preventDefault();
	event.returnValue = "";
});
```

In this example, an event listener is added to the window object. When the user is about to leave the page, the function inside the event listener is executed and the message "Are you sure you want to leave?" is displayed in the browser.

- Resize Event:
  Another common browser event is the resize event. This event is triggered when the browser window is resized. Here is an example of how to handle a resize event:

```javascript
window.addEventListener("resize", function () {
	console.log("Window resized!");
});
```

In this example, an event listener is added to the window object. When the browser window is resized, the function inside the event listener is executed and the message "Window resized!" is logged to the console.

- Scroll Event:
  Another common browser event is the scroll event. This event is triggered when the user scrolls the page. Here is an example of how to handle a scroll event:

```javascript
window.addEventListener("scroll", function () {
	console.log("Page scrolled!");
});
```

In this example, an event listener is added to the window object. When the user scrolls the page, the function inside the event listener is executed and the message "Page scrolled!" is logged to the console.

- Error Event:
  Another common browser event is the error event. This event is triggered when an error occurs while loading a script or an image. Here is an example of how to handle an error event:

```javascript
window.addEventListener("error", function (event) {
	console.log("Error: " + event.message);
});
```

In this example, an event listener is added to the window object. When an error occurs while loading a script or an image, the function inside the event listener is executed and the message "Error: [message]" is logged to the console, where [message] is replaced with the actual error message.

These are just a few examples of the many browser events that can be handled in JavaScript. There are many more events that can be handled, such as the unload event, the hashchange event, the popstate event, the offline event, the online event, the message event, the storage event, and many more.

**_System events:_** are events that are not related to the user or the browser, such as a timer or a server response.

Here are some examples of system events in JavaScript:

- Timeout Event:
  The most common system event in JavaScript is the timeout event. This event is triggered after a specified amount of time. Here is an example of how to handle a timeout event:

```javascript
setTimeout(function () {
    console.log("Timeout!");
}, 1000);
```

In this example, a timeout event is set to trigger after 1 second. When the timeout event is triggered, the function inside the event listener is executed and the message "Timeout!" is logged to the console.


- Interval Event:
  Another common system event is the interval event. This event is triggered repeatedly after a specified amount of time. Here is an example of how to handle an interval event:

```javascript
setInterval(function () {
    console.log("Interval!");
}, 1000);
```

In this example, an interval event is set to trigger every 1 second. When the interval event is triggered, the function inside the event listener is executed and the message "Interval!" is logged to the console.

- Animation Frame Event:
  Another common system event is the animation frame event. This event is triggered before the browser repaints the screen. Here is an example of how to handle an animation frame event:

```javascript
function animate() {
    console.log("Animation frame!");
    requestAnimationFrame(animate);
}

requestAnimationFrame(animate);
```

In this example, an animation frame event is set to trigger before the browser repaints the screen. When the animation frame event is triggered, the function inside the event listener is executed and the message "Animation frame!" is logged to the console.


- Server Response Event:
  Another common system event is the server response event. This event is triggered when the server responds to a request. Here is an example of how to handle a server response event:

```javascript
const request = new XMLHttpRequest();
request.open("GET", "https://example.com");
request.send();

request.addEventListener("load", function () {
    console.log("Server response: " + request.responseText);
});
```

In this example, a server response event is set to trigger when the server responds to a request. When the server response event is triggered, the function inside the event listener is executed and the message "Server response: [response]" is logged to the console, where [response] is replaced with the actual server response.


- Server Error Event:
  Another common system event is the server error event. This event is triggered when the server responds with an error. Here is an example of how to handle a server error event:

```javascript

const request = new XMLHttpRequest();
request.open("GET", "https://example.com");
request.send();

request.addEventListener("error", function () {
    console.log("Server error: " + request.status);
});
```

In this example, a server error event is set to trigger when the server responds with an error. When the server error event is triggered, the function inside the event listener is executed and the message "Server error: [status]" is logged to the console, where [status] is replaced with the actual server error status.


- Server Timeout Event:
  Another common system event is the server timeout event. This event is triggered when the server does not respond within a specified amount of time. Here is an example of how to handle a server timeout event:


## **_Event Listeners:_**

To respond to JavaScript events, you can use event listeners. An event listener is a function that is called when an event occurs. You can attach an event listener to an element using the addEventListener() method. Here is an example of how to attach an event listener to an element:

```javascript
element.addEventListener("click", function () {
    console.log("Element clicked!");
});
```

In this example, an event listener is added to the element. When the element is clicked, the function inside the event listener is executed and the message "Element clicked!" is logged to the console.

You can also attach an event listener to the window object. Here is an example of how to attach an event listener to the window object:

```javascript
window.addEventListener("resize", function () {
    console.log("Window resized!");
});
```

In this example, an event listener is added to the window object. When the browser window is resized, the function inside the event listener is executed and the message "Window resized!" is logged to the console.


## **_Event Object:_**

 JavaScript events have a concept called event propagation, which refers to the order in which events are handled by elements in the DOM tree. When an event occurs on an element, the event is first handled by the element itself, then its parent element, and so on until the event reaches the document object.

There are two types of event propagation: bubbling and capturing. Bubbling is the default propagation type and it means that the event starts at the element where it occurred and then bubbles up the DOM tree. Capturing is the opposite, it starts at the top of the DOM tree and moves down until it reaches the element where the event occurred.
```javascript
const container = document.querySelector('.container');
const button = document.querySelector('button');

container.addEventListener('click', function() {
  alert('Container clicked!');
}, true);

button.addEventListener('click', function() {
  alert('Button clicked!');
}, true);
```

In this example, the event listeners are attached with the true parameter, which means they are using capturing propagation. When the button is clicked, the container event listener is called first, followed by the button event listener.


**Conclusion:**
In summary, JavaScript events are actions or occurrences that happen in the browser, and there are many types of events that can be triggered by the user, the browser, or the system. You can respond to these events using event listeners, which are functions that are called when an event occurs. Additionally, event propagation is an important concept to understand when working with JavaScript events, as it determines the order in which events are handled by elements in the DOM tree.
