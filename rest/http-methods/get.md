
# GET

* The HTTP GET method requests a representation of the specified resource. 

* Requests using GET should only be used to request data (they shouldn't include data).


> Note: Sending body/payload in a GET request may cause some existing implementations to reject the request — while not prohibited by the specification, the semantics are undefined. It is better to just avoid sending payloads in GET requests.

|   Remark  |   |
|  ----  | ----  |
| Request has body |	No |
| Successful response has body |	Yes |
| Safe |	Yes |
| Idempotent |	Yes |
| Cacheable |	Yes |
| Allowed in HTML forms |	Yes |


#### Example
```
HTTP GET http://www.appdomain.com/users
HTTP GET http://www.appdomain.com/users?size=20&page=5
HTTP GET http://www.appdomain.com/users/123
HTTP GET http://www.appdomain.com/users/123/address
```