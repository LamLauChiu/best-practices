# PATCH

* **The HTTP PATCH request method applies partial modifications to a resource.**

* PATCH is somewhat analogous to the **"update"** concept found in  **CRUD   (in general, HTTP is different than CRUD, and the two should not be confused)**.

* **A PATCH request is considered a set of instructions on how to modify a resource.** Contrast this with PUT; which is a complete representation of a resource.

* **A PATCH is not necessarily idempotent, although it can be. Contrast this with PUT; which is always idempotent.** The word "idempotent" means that any number of repeated, identical requests will leave the resource in the same state. For example if an auto-incrementing counter field is an integral part of the resource, then a PUT will naturally overwrite it (since it overwrites everything), but not necessarily so for PATCH.

* **PATCH (like POST) may have side-effects on other resources.**

* **Support for PATCH in browsers, servers, and web application frameworks is not universal. IE8, PHP, Tomcat, Django, and lots of other software has missing or broken support for it.**

* To find out whether a server supports PATCH, a server can advertise its support by adding it to the list in the Allow or Access-Control-Allow-Methods (for CORS) response headers.

* Another (implicit) indication that PATCH is allowed, is the presence of the Accept-Patch header, which specifies the patch document formats accepted by the server.


|   Remark  |   |
|  ----  | ----  |
| Request has body |	Yes |
| Successful response has body |	Yes |
| Safe |	No |
| Idempotent |	No |
| Cacheable |	No |
| Allowed in HTML forms |	No |

<!-- 
#### Example
```
HTTP GET http://www.appdomain.com/users
HTTP GET http://www.appdomain.com/users?size=20&page=5
HTTP GET http://www.appdomain.com/users/123
HTTP GET http://www.appdomain.com/users/123/address
``` -->
<!-- 
https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PATCH -->