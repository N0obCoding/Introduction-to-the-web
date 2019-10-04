# Debugger tools

## Browser Developer Tools

Modern browser (Chrome, Edge, Firefox, Safari, etc...) include a built-in analysis tool for webpages that allow you to view things like the HTML structure, how CSS is being applied, and if there are any Javascript (JS) Errors occurring. These can be accessed with `F12`, `Right Click > Inspect Element`, or through the settings (this differs for each browser). 

When working with HTML/CSS/JS, there are two primary tabs you'll use to debug issues you may be running into - "Inspector" and "Console". 

### The Inspector Tab

The Inspector tab has a section where the HTML structure for the page is displayed, and a section where the selected HTML element's CSS is displayed. 

Within the CSS panel, you can toggle if a property is displayed, add new CSS properties to see how it will affect your page live, and even edit existing properties. It's important to note that these changes are **local to your browser** and not being saved to the document, so refreshing the page or navigating to a new URL will reset any changes you have in place. 

### The Console Tab

When it comes to JS, the console is a great place to test code! Some ways to test code in the console:

- Adding `console.log("message")` messages to your code to indicate when you hit that line of code
- Typing directly into the console and seeing the output live
- Errors will appear in the console including a trace back to where the error originated from

### Responsible Preview/Mobile Preview

Some browsers offer the ability to preview what a page would look like in sizes other than your window's size, including presets for various mobile devices to help debug visual issues on those devices. `Ctrl + Shift + M` will toggle on/off responsive view in Chrome and Firefox. 

# Contributors
[Tyler VanBlargan](https://github.com/12vanblart)
