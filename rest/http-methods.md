# Interaction Design with HTTP methods

#### Request Methods
<!-- 
![alt request-methods.png](../src/images/request-methods.png"request-methods.png") -->


<!-- GET
The GET method requests a representation of the specified resource. Requests using GET should only retrieve data.
HEAD
The HEAD method asks for a response identical to that of a GET request, but without the response body.
POST
The POST method is used to submit an entity to the specified resource, often causing a change in state or side effects on the server.
PUT
The PUT method replaces all current representations of the target resource with the request payload.
DELETE
The DELETE method deletes the specified resource.
CONNECT
The CONNECT method establishes a tunnel to the server identified by the target resource.
OPTIONS
The OPTIONS method is used to describe the communication options for the target resource.
TRACE
The TRACE method performs a message loop-back test along the path to the target resource.
PATCH
The PATCH method is used to apply partial modifications to a resource. -->


|  Request Methods   | semantics  |
|  ----  | ----  |
| GET  | The GET method requests a representation of the specified resource. Requests using GET should only retrieve data. |
| HEAD  | The HEAD method asks for a response identical to that of a GET request, but without the response body. |
| POST  | The POST method is used to submit an entity to the specified resource, often causing a change in state or side effects on the server. |
| PUT  | The PUT method replaces all current representations of the target resource with the request payload. |
| DELETE  | The DELETE method deletes the specified resource. |
| CONNECT  | The CONNECT method establishes a tunnel to the server identified by the target resource. |
| OPTIONS  | The OPTIONS method is used to describe the communication options for the target resource. |
| TRACE  | The TRACE method performs a message loop-back test along the path to the target resource. |
| PATCH  | The PATCH method is used to apply partial modifications to a resource.|


#### HTTP Methods for RESTful APIs between CRUD

|HTTP Method |	CRUD	|Entire Collection (e.g. /users)	|Specific Item (e.g. /users/123)|
|  ----  | ----  |  ----  | ----  |
|POST|	Create|	201 (Created), ‘Location’ header with link to /users/{id} containing new ID.	|Avoid using POST on single resource|
|GET|	Read|	200 (OK), list of users. Use pagination, sorting and filtering to navigate big lists.	|200 (OK), single user. 404 (Not Found), if ID not found or invalid.|
|PUT|	Update/Replace|	405 (Method not allowed), unless you want to update every resource in the entire collection of resource.	|200 (OK) or 204 (No Content). Use 404 (Not Found), if ID not found or invalid.|
|PATCH|	Partial Update/Modify|	405 (Method not allowed), unless you want to modify the collection itself.	|200 (OK) or 204 (No Content). Use 404 (Not Found), if ID not found or invalid.|
|DELETE|	Delete|	405 (Method not allowed), unless you want to delete the whole collection — use with caution.	|200 (OK). 404 (Not Found), if ID not found or invalid.|


