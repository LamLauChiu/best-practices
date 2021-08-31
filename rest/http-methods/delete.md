# DELETE

* **The HTTP DELETE request method deletes the specified resource.**

* Requests using GET should only be used to request data (they shouldn't include data).


|   Remark  |   |
|  ----  | ----  |
| Request has body |		May |
| Successful response has body |		May |
| Safe |	No |
| Idempotent |	Yes |
| Cacheable |	No |
| Allowed in HTML forms |	No |

#### Example
```
HTTP DELETE http://www.appdomain.com/users/123
HTTP DELETE http://www.appdomain.com/users/123/accounts/456
```

<!-- https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/DELETE -->