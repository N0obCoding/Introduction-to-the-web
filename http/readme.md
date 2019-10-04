# HyperText Transfer Protocol (HTTP)

HTTP is a protocol that **defines how client and server communicates**. 

*Click [here](https://github.com/N0obCoding/Introduction-to-the-web/tree/master/clientServer) to Learn About Client-Server Model.*

Every time we search up something with our browser, let say Wikipedia, the browser will then communicate with Wikipedia's server to get the resources you had asked for.

Let's see how the communication process works.
  1. The **Browser sends the request** for resources to the server. (in the form of URL)
  2. The **Server process the request**, then **respond** accordingly to it.
  
### Examples
**Request** and **Response** are the keywords in HTTP. To make it easier, imagine the communication between server and client as a conversation between a Customer and a Waiter.

A customer would request **his/her favourite meal** then the waiter have to **produce the meal** based on the request made and **respond to the customer with the meal** different customer may request for different meal, so the waiter have to respond accordingly too.

But what if the waiter is requested for a meal the restaurant doesn't provide? Commonly, the bartender would have to tell the customer the meal is currently unavailable. So, similarly, the server should tell us that the web page is unavailable, which is why we see 'ERROR 404' sometimes. If you have not met this situation before, click on the link https://github.com/thisPageDon'tExist

After clicking the link, you should see an Error 404 page, which is Github Server telling you that the page you requested for is unavailable.

## Request Methods
We can see that the request involved in the above explanation is about getting resources, this request method is known as **GET**. However, there are few other request methods can be utilized. Below listed request method are among the most commonly used.
  1. **GET**
  2. **POST**
  
### GET
Every time we try to load a page, we are actually utilizing GET method. As the name suggested, this method helps us to fetch data from the server.

### POST
Every time we are trying to submit something to the server (Examples: Facebook Post, Tweet), we are using the POST method. This method helps us to send informations to the server.

## Response Code
Response Code are formed in 3 digits, the first digit indicate the type of the response. Below are the 5 types of Response Code. Response Code reveals information about the request made, whether it's success, failed or changed.

  * 1xx : Informational Response
  * 2xx : Success
  * 3xx : Redirection
  * 4xx : Client Errors
  * 5xx : Server Errors


# Contributors
RichardLim00
