# CONNECT

* **The HTTP CONNECT method starts two-way communications with the requested resource. It can be used to open a tunnel.**

* For example, the CONNECT method can be used to access websites that use SSL (HTTPS). The client asks an HTTP Proxy server to tunnel the TCP connection to the desired destination. The server then proceeds to make the connection on behalf of the client. Once the connection has been established by the server, the Proxy server continues to proxy the TCP stream to and from the client.

> CONNECT is a hop-by-hop method.

|   Remark  |   |
|  ----  | ----  |
| Request has body |	No |
| Successful response has body |	Yes |
| Safe |	No |
| Idempotent |	No |
| Cacheable |	No |
| Allowed in HTML forms |	No |


<!-- Example request URIs:
```
HTTP GET http://www.appdomain.com/users
HTTP GET http://www.appdomain.com/users?size=20&page=5
HTTP GET http://www.appdomain.com/users/123
HTTP GET http://www.appdomain.com/users/123/address
``` -->

####  Syntax
```javascript
CONNECT www.example.com:443 HTTP/1.1
```

#### Example

* Some proxy servers might need authority to create a tunnel. See also the Proxy-Authorization header.

```javascript
CONNECT server.example.com:80 HTTP/1.1
Host: server.example.com:80
Proxy-Authorization: basic aGVsbG86d29ybGQ=
```