# The Document Object Model (DOM)

# What is the DOM?
The DOM (Document Object Model) is an API (Application Programming Interface) that provides a browser’s representation of a parsed HTML or XML document. Its properties and methods may be accessed or manipulated using JavaScript to change a document’s structure, content, and style.

In other words, through use of the DOM, a protocol is established, and this standard allows developers to use JavaScript to dynamically access and update documents.


If this sounds difficult to understand, you can view it like this: the DOM is a way that you (and your browser) can represent the entire HTML or XML page, that looks pretty much like a tree. Let's imagine a basic html page. The tree is your page. You have a branch called "body". Let's say you used several "section" tags nested within your "body" tag. You can view each of those "section" tags as a branch growing on your "body" branch. Thanks to this tree-like representation of the webpage, we can then select the exact branch we want and do things with it. 

# Why use the DOM?
Specifically, developers may use JavaScript and the DOM to:

1. Get, add, remove, and reorder HTML elements.
2. Get, add, remove, and update text content inside HTML elements.
3. Get, set, and remove attributes of HTML elements in a page.
4. Add and remove event-triggered functions to HTML elements.

In JavaScript, you may access an object’s methods and properties using dot notation.

If you see code that looks like this: document.getSomething(moreWords), the "document" part is the object, the "getSomething" is the method, the "moreWords" is the argument.

Objects are an important javascript concept that you might be interested in refining later. For the purpose of this document, assuming you don't know anything else about objects, think of methods as a kind of function, defined to be used on a specific object. Here you don't have to do the defining, you can just use those that already exist to grab the branches you need in the DOM tree. The object we are manipulating here is "document", so your HTML or XML webpage.

Let's see some ways to do just that.

# Dom manipulations

Get an element by ID:
```
document.getElementById(‘yourElementID’);
```

Document is the object, in this case the web page you want something from, and the dot is used to access its method (getElementById), and then you may pass the ID as an argument to this method. 

Pay attention to "element" : here it is written in the singular. This is not the case for the other ways you can use to access the DOM, where we use the plural form. Using "getElementById" will return only one "branch" from the tree as we discussed above. Other ways of accessing the DOM will return more than one.

Get elements by class name:
```
document.getElementsByClassName(‘yourElementClass’);
```
As mentioned just above, this is a way of grabbing things from your webpage that can return more than one item. If you have used the class "purple" twice in your webpage, this snippet of code will catch both of those instances. They will automatically be given a number, by the order in which they are encountered in the webpage code when you read if from top to bottom. The first one encountered in the webpage will be 0. The second one will be 1, then 2 etc.

Get the first element of class name:
```
document.getElementsByClassName(‘yourElementClass’)[0];
```

Get elements by tag:
```
document.getElementsByTagName(‘p’);
```

Get the first element of tag:
```
document.getElementsByTagName(‘p’)[0];
```

Get an element matching CSS selector:
```
document.querySelector(‘#myContainer .myClass button’);
```
Pay special attention to whether your selector is a class (starts with a . in your CSS) or an id (starts with a # in your CSS) when you're selecting based on CSS. Include those symbols in the argument you pass.

Get all elements matching CSS selector:
```
document.querySelectorAll(‘.myClassToSelect’);
```

You may store elements as variable values, to possibly make your JavaScript more readable although this is optional:
```
const button = document.querySelector(‘.button’);
```
You may also get the text content from inside an HTML element.

Get the text content inside the page’s heading:
```
document.querySelector(‘.button’).textContent;
```
Another way to do this is to use the .innerText method, but the latter won't grab the text between <script> or <style> tags.

Or use a variable
```
const button = document.querySelector(‘.button’);
button.textContent;
```

Update the text content
```
document.getElementById(‘yourElementID’).textContent = ‘Learning about the DOM’;
```

Remove the text content of an element
```
document.getElementById(‘yourElementID’).textContent = ‘’;
```
You’re not just limited to classes, IDs, tags, and text content. You may work with any HTML element’s attributes.

Get the src URL of an image
```
const img = document.getElementById(‘yourImageId’);
img.getAttribute(‘src’);
```

Update the src URL of an image
```
const img = document.getElementById(‘yourImageId’);
const newSrc = ‘https://via.placeholder.com/150’;
img.setAttribute(‘src’, newSrc);
```

Remove the src URL of an image
```
const img = document.getElementById(‘yourImageId’);
img.removeAttribute(‘src’);
```

One of the DOM’s most powerful features is the ability to define events. There are many types of DOM events built-in for developers to use. Here are some of the most popular:

* ```click``` - when a pointing device is pressed and released on an element
* ```mousedown``` - when a pointing device is pressed down on an element
* ```mouseenter``` - when a pointing device moves onto an element
* ```mouseout``` - when a pointing device moves off an element
* ```mouseover``` - triggered persistently whilst a pointing device moves over an element
* ```keydown``` - a key is pressed down
* ```keyup``` - a key is released
* ```Input``` - an element’s value changes. The element has the contenteditable HTML attribute

There are many more events which you may read about further here: 
https://developer.mozilla.org/en-US/docs/Web/Events

You shall usually attach events to HTML elements, then define functions that contain logic that ought to happen when said events are triggered.

# Your first JavaScript DOM Event
```
const element = document.getElementById(‘myElement’);

element.addEventListener(‘click’, () => {
	alert(‘clicked!’);
});
```

Without arrow functions, this may be expressed as:
```
element.addEventListener(‘click’, function() {
	alert(‘clicked!’);
});
```

If that code confuses you, take away the variable and arrow function:

```
document.getElementById(‘myElement’).addEventListener(‘click’, function() {
	alert(‘clicked!’);
});
```
So, we are telling JavaScript the following.

1. Get the element with the id of ‘myElement’
2. Add an event listener for the ‘click’ event
3. When this happens, alert ‘clicked’ to the user

Here you can see two chained DOM methods in use together, and also the use of a function inside of a function. This is known as a callback.

Before you can learn the final most common piece of the DOM that developers use, you should understand how the browser represents our documents in some greater detail.

The DOM views documents as a node-tree. And just like in HTML elements, DOM ‘nodes’ have parent, child, and sibling relationships. That’s why it may be helpful to think of the DOM as a tree.

You may view the DOM whenever you like by opening your browser’s developer tools and inspecting HTML. Use the ‘Elements’ tab to view the node-tree of your document.

Consider a div with the ID of ‘myElement’, and this div contains a paragraph of text.

We can select this similar to how we did before, but we don’t need to assign a class or ID to the element that we wish to target:

Get the text content of the paragraph tag we mentioned before
```
document.getElementById(‘myElement’).firstElementChild.textContent;
```

This is another abstraction that the DOM provides that makes it easy to access elements in your documents using JavaScript.

There are many more DOM properties that we can use to move around the DOM. You will often hear this referred to as DOM traversal, or ‘walking the DOM’. A more in-depth resource highly recommended would be the Mozilla Developer Network’s free resource which you may access and bookmark for future reference.

https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model

Now you should realistically have the knowledge and resources to find, save, and act when almost any event occurs on any given element, the last piece now is to understand how to remove and add elements to the DOM tree.

Removing elements can be quite simple. You select an element (and may wish to store it) then you may use the remove method.
```
document.getElementById(‘elementToRemove’).remove();
```

However, unfortunately this method has limited browser support. As a precaution, you may prefer to use the older ```.removeChild()``` method. This would naturally involved selecting the element’s parent rather than the element to be removed, then passing the element to remove as an argument to that method.

Now to add an element to the DOM, we just select a DOM element, create a new element, then add it to the DOM either before, after, or inside the first element we selected.

Consider the following code:

```
// get an unordered list from our document
const list = document.getElementsByTagName(‘ul’)[0];

// create a list item
const li = document.createElement(‘li’);

// set its text content
li.textContent = ‘Look, I added an element to the DOM!’;

// add it to the list we selected before
list.appendChild(li);
```

There is a further range of methods such as ```.insertBefore()``` and ```.insertAfter()```  available for inserting elements in your documents, and again I would recommend you read further into this on the Mozilla Developer Network if you wish to learn more about this.

Once you play around with these DOM basics for a while, try browsing around the web again, and consider just how many amazing possibilities you can already achieve with what you have learned about the DOM.

# Contributors
[Carl Evans](https://github.com/carl-evans)

### License

This work is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License. To view a copy of this license, visit [http://creativecommons.org/licenses/by-sa/4.0/](http://creativecommons.org/licenses/by-sa/4.0/).

