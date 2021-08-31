# PUT

* **The HTTP PUT request method creates a new resource or replaces a representation of the target resource with the request payload.**

* The difference between PUT and POST is that PUT is idempotent: calling it once or several times successively has the same effect (that is no side effect), whereas successive identical POST requests may have additional effects, akin to placing an order several times.


|   Remark  |   |
|  ----  | ----  |
| Request has body |	Yes |
| Successful response has body |    No |
| Safe |		No |
| Idempotent |	Yes |
| Cacheable |	No |
| Allowed in HTML forms |	No |

#### Example
Example request URIs:
```
HTTP PUT http://www.appdomain.com/users/123
HTTP PUT http://www.appdomain.com/users/123/accounts/456
```
<!-- 
https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PUT -->