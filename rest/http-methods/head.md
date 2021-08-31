# HEAD

* The HTTP HEAD method requests the headers that would be returned if the HEAD request's URL was instead requested with the HTTP GET method. 

* For example, if a URL might produce a large download, a HEAD request could read its Content-Length header to check the filesize without actually downloading the file.

> Warning:
A response to a HEAD method should not have a body. If it has one anyway, that body must be ignored: any representation headers that might describe the erroneous body are instead assumed to describe the response which a similar GET request would have received.

* If the response to a HEAD request shows that a cached URL response is now outdated, the cached copy is invalidated even if no GET request was made.


|   Remark  |   |
|  ----  | ----  |
| Request has body |	No |
| Successful response has body |	No |
| Safe |	Yes |
| Idempotent |	Yes |
| Cacheable |	Yes |
| Allowed in HTML forms |	No |


<!-- Example request URIs:
```
HTTP GET http://www.appdomain.com/users
HTTP GET http://www.appdomain.com/users?size=20&page=5
HTTP GET http://www.appdomain.com/users/123
HTTP GET http://www.appdomain.com/users/123/address
``` -->