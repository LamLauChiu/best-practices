# Idempotent REST APIs


#### What is Idempotent

> An idempotent HTTP method is an HTTP method that can be called many times without different outcomes. It would not matter if the method is called only once, or ten times over. The result should be the same.

> Idempotence essentially means that the result of a successfully performed request is independent of the number of times it is executed. For example, in arithmetic, adding zero to a number is an idempotent operation.


* **Calling it once or several times successively has the same effect (that is no side effect)**

* **All safe methods are also idempotent.**


#### Idempotency with HTTP Methods

* **POST, CONNECT is NOT idempotent.**
* **GET, PUT, DELETE, HEAD, OPTIONS and TRACE are idempotent.**



##### HTTP POST
Generally – not necessarily – POST APIs are used to create a new resource on server. So when you invoke the same POST request N times, you will have N new resources on the server. So, POST is not idempotent.

```javascript
POST /add_row HTTP/1.1 is not idempotent; if it is called several times, it adds several rows:

POST /add_row HTTP/1.1
POST /add_row HTTP/1.1   -> Adds a 2nd row
POST /add_row HTTP/1.1   -> Adds a 3rd row
```
##### HTTP GET, HEAD, OPTIONS and TRACE
GET, HEAD, OPTIONS and TRACE methods NEVER change the resource state on server. 

They are purely for retrieving the resource representation or meta data at that point of time. So invoking multiple requests will not have any write operation on server, so GET, HEAD, OPTIONS and TRACE are idempotent.
```javascript
GET /pageX HTTP/1.1 is idempotent. Called several times in a row, the client gets the same results:

GET /pageX HTTP/1.1
GET /pageX HTTP/1.1
GET /pageX HTTP/1.1
GET /pageX HTTP/1.1
```

##### HTTP PUT
Generally – not necessarily – PUT APIs are used to update the resource state. 

If you invoke a PUT API N times, the very first request will update the resource; then rest N-1 requests will just overwrite the same resource state again and again – effectively not changing anything. Hence, PUT is idempotent.

##### HTTP DELETE
When you invoke N similar DELETE requests, first request will delete the resource and response will be 200 (OK) or 204 (No Content). Other N-1 requests will return 404 (Not Found). 

Clearly, the response is different from first request, but there is no change of state for any resource on server side because original resource is already deleted. So, DELETE is idempotent.

```javascript
DELETE /idX/delete HTTP/1.1 is idempotent, even if the returned status code may change between requests:

DELETE /idX/delete HTTP/1.1   -> Returns 200 if idX exists
DELETE /idX/delete HTTP/1.1   -> Returns 404 as it just got deleted
DELETE /idX/delete HTTP/1.1   -> Returns 404
```