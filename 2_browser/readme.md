<p style="center">
    <link rel="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" type="text/css">
    <i class="fa fa-lg fa-safari"></i>
    <i class="fa fa-lg fa-chrome"></i>
    <i class="fa fa-lg fa-firefox"></i>
    <i class="fa fa-lg fa-edge" aria-hidden="true"></i>
    <i class="fa fa-lg fa-internet-explorer"></i>
</p>

# **Understanding the Browser**
A browser is a client-side application that enables users to access resources that are hosted on the internet. It serves as the gateway between the user and the Web, and it has the responsibility of allowing the user to interact with the websites and web applications, mainly through HTTP requests.

> In relation to the previous module, the browser is the **client** in the **client-server** model. It is responsible for sending requests to a server (or servers) in the network and handling the responses so that the user can be presented with information in a human-friendly manner.

Browsers are capable of fetching and interpreting different resources, for example HTML documents, images, videos, and PDF files. Additionally, Browsers know how to compose, arrange and style a large number of resources and assets, and to visually compose what the user sees.

## The evolution of the Web Browser
In the last few years, browsers have evolved from being a simple interface that requests some static files from a server, and draw the results in a window, to a more complex echosystem of tools and components that allow for more complex and dynamic applications to be consumed by the end-users.

 Below we can see the [Netscape Navigator](https://en.wikipedia.org/wiki/Netscape_(web_browser)), one of the first widely used web browsers.

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/en/3/39/Welcome_to_Netscape.gif" width="300">
</p>

~~Every resource that is hosted on the internet has a unique id which is called as Uniform resource Identifier.~~

~~There are different versions of browsers available for different sizes of devices such as mobiles and desktops.~~

**Disclaimer**: In the interest of simplicity for the scope of this course, the above is an overly simplified description of the browser. As we progress through the course, we will continue to understand the power behind these applications.

## **How does a web browser work?**

Now, we have understood what a browser is. But that's not enough. So, now let's understand the internal functioning of it.

First, whenever you enter the url in the address bar and hit enter then the browser sends the request to something that is called as a Domain Name Server shortly called as DNS. So what's a DNS?

### Domain Name Server :
It is similar to the phonebook that we would use in the early days. It basically consists of a list of people and their corresponding phone numbers. It is same with the DNS but here we have the domain names and their corresponding ip address.

DomainName | IPAddress
---------- | ---------
google.com | 172.217.14.238 
github.com | 192.30.255.112

Now the responsibilty of the DNS server is to look up the domain name that is requested by the browser i.e user in the list and return the corresponding ip address.

Back to the browser again. Now the response that is send by the DNS server is received by the browser and now browser sends a request asking for the resource that is hosted on that particular address on the internet.The server sends the requested resource to the browser.

Now, the browser renders the resource by using certain languages. They are:

**1) HTML :** HTML stands for Hypertext Markup Language. This language consists of several html tags.The browser uses this tags to identify the type of content and how to display it.

**2) CSS :** CSS stands for Cascading Style Sheets. CSS is used to specify how the content should be displayed on the web page.

**3) JS :** JS stands for Javascript. JS is used to make the web page to respond to user actions. Every web browser has a dedicated javascript engine. V8 is google chrome's javascript engine, Spider Monkey is the javascript engine of Mozilla Firefox, Chakra is the javascript engine of Microsoft Edge.

This is the basic overview of a web browser. Apart from this, web browser consists of various debugging tools and utilities to test the performance of the website and the browser.

## Different Browsers, different worlds

Different browsers that are developed by different companies such as Google Chrome, Mozilla Firefox, Apple's Safari, and Microsoft's Internet Explorer and Edge.

Allthough many browsers have a very similar set of features, the implementation by each company is often differrent. For our users, this can result in a different experience when interacting with our applications.

You, as a Software Developer, are responsible of understanding the capabilities and limitations that each browser has, and work around them so that your users can have a seamless experience across different browsers.

# Key Take-away points
* The Browser allows users to _interact with resources in the web_
* The Browser acts as the _client_, **requesting** resources from the server.

## Up next: [The Document Object Model (DOM)](../3_dom/readme.md)


# Contributors
* [Daniel Ormeno](https://github.com/DanielOrmeno)
* [Rohit Arram](https://github.com/rohit1636)
