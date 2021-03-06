- **Author:** [[Tania Rascia]]
- **Tags:**  #HTML #JavaScript #[[Book Highlights]]
- **Source:** #MoonReader
- ---
- ## Introduction
    - the web browser provides an API for accessing the HTML document in a tree structure known as the Document Object Model (DOM).
    - In order to be a proficient web developer, having a deep understanding of what the DOM is and how to work with it is essential
- ## Introduction to the DOM
    - JavaScript is the client-side scripting language that connects to the DOM in an internet browser.
    - the DOM is language agnostic, or created to be independent from a particular programming language
    - JavaScript’s implementation of the HTML DOM.
    - the browser creates a representation of the document known as the Document Object Model.
    - This model allows JavaScript to access the text content and elements of the website document as objects.
    - The document
    - object is a built-in object that has many properties and methods that we can use to access and modify websites
        - What is the Difference Between the DOM and HTML Source Code?
        - The DOM is modified by client-side JavaScript
    - The browser automatically fixes errors in the source code
        - The DOM is modified by client-side JavaScript
    - The browser automatically fixes errors in the source code
        - For more in-depth information on the DOM, review the Document Object Model (DOM) page on the Mozilla Developer Network.
- ## Understanding the DOM Tree and Nodes
    - The DOM is often referred to as the DOM tree, and consists of a tree of objects called nodes.
    - Home
    - Here we have an anchor element, which is a link to index.html.
        - a is the tag
        - href is the attribute
        - index.html is the attribute value
    - Home is the text.
        - instead of typing that object and method every time we want to access the nav link, we can place the element into a variable to work with it more easily.
        - All items in the DOM are defined as nodes. There are many types of nodes, but there are three main ones that we work with most often:
    - Element nodes
    - Text nodes
    - Comment nodes
        - When an HTML element is an item in the DOM, it is referred to as an element node.
        - Any lone text outside of an element is a text node,
        - HTML comment is a comment node.
        - the document itself is a document node, which is the root of all other nodes.
        - tree structure of nested nodes, which is often referred to as the DOM tree.
        - Note: When working with an HTML-generated DOM, the indentation of the HTML source code will create many empty text nodes, which won’t be visible from the DevTools Elements tab.
        - Read about Whitespace in the DOM
        - Every node in a document has a node type, which is accessed through the nodeType property.
        - This is a very handy way to access the currently active element in Developer Tools by typing $0.
        - In addition to nodeType, you can also use the nodeValue property to get the value of a text or comment node, and nodeName to get the tag name of an element.
        - An event in JavaScript is an action the user has taken.
        - An event in JavaScript is an action the user has taken.
- ## How To Access Elements in the DOM
    - In order to be proficient at accessing elements in the DOM, it is necessary to have a working knowledge of CSS selectors, syntax and terminology as well as an understanding of HTML elements.
    - Accessing an element by ID is an effective way to get an element quickly in the DOM.
    - an ID must always be unique to the page, and therefore you will only ever be able to access a single element at a time with the getElementById() method.
    - We can get all the elements with a given class name with the getElementsByClassName() method.
    - instead of just getting one element, we have an array-like object of elements.
    - for (i = 0; i < demoClass.length; i++) {
    - demoClass[i].style.border = '1px solid orange';
    - }
        - Just like accessing an element by its class, getElementsByTagName() will return an array-like object of elements
        - To access a single element, we will use the querySelector() method.
        - querySelector() will return the first element that matches the query
        - We can use the querySelectorAll() method to collect all the elements that match a specific query.
        - Using the forEach() method, we can apply the color green to the border property of all matching elements. (loop through object)
- ## How To Traverse the DOM
    - Often, you will want to move through the DOM without specifying each and every element beforehand.
    - The nodes in the DOM are referred to as parents, children, and siblings, depending on their relation to other nodes.
    - how can we get the grandparent, which is two levels above? We can do so by chaining properties together.
    - p.parentNode.parentNode;
    - The childNodes property will return a live list of every child of a node
    - This is not intuitive, as the Elements tab of DevTools strips out white space nodes.
        - When doing basic DOM manipulation such as in this example, the element-specific properties are extremely helpful.
        - childNodes
    - and children
    - do not return arrays with all the Array properties and methods, but they appear and behave similarly to JavaScript arrays
        - Sibling Nodes
    - The siblings of a node are any node on the same tree level in the DOM. Siblings do not have to be the same type of node - text, element, and comment nodes can all be siblings.
        - Since we created our DOM from scratch and not as a JavaScript web app, we will need to use the element sibling properties to access the previous and next element nodes, as there is white space in the DOM
        - Sibling properties can be chained together, just like parent and node properties.
- ## How To Make Changes to the DOM
    - Inserting Nodes into the DOM
    - The methods appendChild()
    - and insertBefore()
    - are used to add items to the beginning, middle, or end of a parent element, and replaceChild()
    - is used to replace an old node with a new node.
        - createElement()
    - only creates one element and cannot be reused.
        - With a combination of appendChild()
    - , insertBefore()
    - , and replaceChild()
    - , you can insert nodes and elements anywhere in the DOM.
        - Child nodes can be removed from a parent with removeChild(), and a node itself can be removed with remove().
        - Another method you may see for removing child elements from the DOM is setting the innerHTML property of a parent element to an empty string (""). This is not the preferred method because it is less explicit
- ## How To Modify Attributes, Classes, and Styles in the DOM
    - Until recently, a popular JavaScript library called jQuery was most often used to select and modify elements in the DOM.
    - The querySelector() method is more robust in that it can select an element on the page by any type of selector.
    - However, when accessing multiple elements by a common selector, such as a specific class, we have to loop through all the elements in the list.
    - The methods getElementsByClassName() and getElementsByTagName() will return HTML collections which do not have access to the forEach() method that querySelectorAll() has.
    - In JavaScript, we have four methods for modifying element attributes:
    - The hasAttribute() and getAttribute() methods are usually used with conditional statements, and the setAttribute() and removeAttribute() methods are used to directly modify the DOM.
    - the classList property, which comes with a few helpful methods. These methods are similar to the jQuery addClass, removeClass, and toggleClass methods.
    - Unlike in the className example, using classList.add() will add a new class to the list of existing classes.
    - It is also possible to use setAttribute to modify the class of an element.
    - this will remove all existing inline styles from the element. Since this is likely not the intended effect, it is better to use the style attribute directly
    - If many stylistic changes are to be applied to an element, the best course of action is to apply the styles to a class and add a new class.
    - HTML elements often have additional information assigned to them in the form of attributes. Attributes may consist of name/value pairs, and a few of the most common attributes are class and style.
- ## Understanding Events in JavaScript
    - Events are actions that take place in the browser that can be initiated by either the user or the browser itself.
    - The page finishes loading
    - The user clicks a button
    - The user hovers over a dropdown
    - The user submits a form
    - The user presses a key on their keyboard
        - An event handler is a JavaScript function that runs when an event fires.
        - An event listener attaches a responsive interface to an element, which allows that particular element to wait and “listen” for the given event to fire.
        - There are three ways to assign events to elements: - Inline event handlers - Event handler properties - Event listeners
        - Inline Event Handler Attributes
        - Inline event handlers are a straightforward way to begin understanding events, but they generally should not be used beyond testing and educational purposes.
        - Inline event handlers are a straightforward way to begin understanding events, but they generally should not be used beyond testing and educational purposes.
        - You can compare inline event handlers to inline CSS styles on an HTML element. It is much more practical to maintain a separate stylesheet of classes than create inline styles on every element, just as it is more feasible to maintain JavaScript that is handled entirely through a separate script file than add handlers to every element.
        - // Add event handler as a property of the button element
    - const button = document.querySelector('button');
    - button.onclick = changeText;
        - Note: Event handlers do not follow the camelCase convention that most JavaScript code adheres to. Notice that the code is onclick, not onClick.
        - Note that when passing a function reference to the onclick property, we do not include parentheses, as we are not invoking the function in that moment, but only passing a reference to it.
        - The event handler property is slightly more maintainable than the inline handler, but it still suffers from some of the same hurdles.`
        - ```javascript
javascript  // Events can be overwritten 
button.onclick = changeText;
button.onclick = alertText;  ```
    - ### Attachments area
        - The latest addition to JavaScript event handlers are event listeners.
        - An event listener watches for an event on an element. Instead of assigning the event directly to a property on the element, we will use the addEventListener() method to listen for the event.
        - addEventListener() takes two mandatory parameters — the event it is to be listening for, and the listener callback function.
        - event listeners seem very similar to event handler properties, but they have a few advantages. We can set multiple event listeners on the same element,
        - Event listeners are currently the most common and preferred way to handle events in JavaScript.
        - A click is a compound event that is comprised of combined mousedown and mouseup events, which fire when the mouse button is pressed down or lifted, respectively.
        - Focus is achieved when an element is selected, for example, through a mouse click or navigating to it via the TAB key.
        - Although they look similar, keydown and keypress events do not access all the exact same keys. While keydown will acknowledge every key that is pressed, keypress will omit keys that do not produce a character, such as SHIFT, ALT, or DELETE.
        - If a parameter, known as an event object, is passed through to the event listener, we can access more information about the action that took place.
        - Note that keyCode is in the process of being deprecated and it is preferable to use code in new projects.
        - Event Objects
        - The Event object consists of properties and methods that all events can access.
        - The Event object is passed through a listener function as a parameter. It is usually written as event or e.
        - using event.target. This is extremely useful, as it allows you to place only one event listener that can be used to access many nested elements. 
