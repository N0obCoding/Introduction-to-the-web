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
  3. **PUT**
  4. **DELETE**  
### GET
Every time we try to load a page, we are actually utilizing GET method. As the name suggested, this method helps us to fetch data from the server.

### POST
Every time we are trying to submit something to the server (Examples: Facebook Post, Tweet), we are using the POST method. This method helps us to send informations to the server.

### PUT
Use PUT APIs primarily to update existing resource (if the resource does not exist then API may decide to create a new resource or not). If a new resource has been created by the PUT API, the origin server MUST inform the user agent via the HTTP response code 201 (Created) response and if an existing resource is modified, either the 200 (OK) or 204 (No Content) response codes SHOULD be sent to indicate successful completion of the request.

If the request passes through a cache and the Request-URI identifies one or more currently cached entities, those entries SHOULD be treated as stale. Responses to this method are not cacheable.

### Difference between POST and PUT
The difference between the POST and PUT APIs can be observed in request URIs. POST requests are made on resource collections whereas PUT requests are made on an individual resource.

### DELETE
As the name applies, DELETE APIs are used to delete resources (identified by the Request-URI).

A successful response of DELETE requests SHOULD be HTTP response code 200 (OK) if the response includes an entity describing the status, 202 (Accepted) if the action has been queued, or 204 (No Content) if the action has been performed but the response does not include an entity.

DELETE operations are idempotent. If you DELETE a resource, it’s removed from the collection of resource. Repeatedly calling DELETE API on that resource will not change the outcome – however calling DELETE on a resource a second time will return a 404 (NOT FOUND) since it was already removed. Some may argue that it makes DELETE method non-idempotent. It’s a matter of discussion and personal opinion.

## Response Code
Response Code are formed in 3 digits, the first digit indicate the type of the response. Below are the 5 types of Response Code. Response Code reveals information about the request made, whether it's success, failed or changed.

  * 1xx : Informational Response
	* 100 Continue
		This interim response indicates that everything so far is OK and that the client should continue the request, or ignore the response if the request is already finished.

	* 101 Switching Protocol
		This code is sent in response to an Upgrade request header from the client, and indicates the protocol the server is switching to.
	
	* 102 Processing (WebDAV)
		This code indicates that the server has received and is processing the request, but no response is available yet.
	
	* 103 Early Hints
		This status code is primarily intended to be used with the Link header, letting the user agent start preloading resources while the server prepares a response.

  * 2xx : Success
	* 200 OK
		The request has succeeded. The meaning of the success depends on the HTTP method:
			GET: The resource has been fetched and is transmitted in the message body.
			HEAD: The entity headers are in the message body.
			PUT or POST: The resource describing the result of the action is transmitted in the message body.
			TRACE: The message body contains the request message as received by the server

	* 201 Created
		The request has succeeded and a new resource has been created as a result. This is typically the response sent after POST requests, or some PUT requests.

	* 202 Accepted
 		The request has been received but not yet acted upon. It is noncommittal, since there is no way in HTTP to later send an asynchronous response indicating the outcome of the request. It is intended for cases where another process or server handles the request, or for batch processing.

	* 203 Non-Authoritative Information
 		This response code means the returned meta-information is not exactly the same as available from the origin server, but collected from a local or a third-party copy. This is mostly used for mirrors or backups of another resource. Except for that specific case, 200 OK response should be preferred instead of this status.

	* 204 No Content
 		There is no content to send for this request, but the headers may be useful. The user-agent may update its cached headers for this resource with the new ones.

	* 205 Reset Content
		Tells the user-agent to reset the document which sent this request.

	* 206 Partial Content
		This response code is used when the Range header is sent from the client to request only part of a resource.

  * 3xx : Redirection
  * 4xx : Client Errors
  * 5xx : Server Errors


## Contributors
RichardLim00
mrnoob4

### License

This work is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License. To view a copy of this license, visit [http://creativecommons.org/licenses/by-sa/4.0/](http://creativecommons.org/licenses/by-sa/4.0/).

