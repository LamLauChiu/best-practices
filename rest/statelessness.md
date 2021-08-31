
# Statelessness in REST APIs 

* As per the REST (REpresentational **“State”** Transfer) architecture, **the server does not store any state about the client session on the server-side**. 

* This restriction is called **Statelessness**.


* **Client is responsible for storing and handling all application state-related information on client side**.

> Statelessness means that every HTTP request happens in complete isolation. When the client makes an HTTP request, it includes all information necessary for the server to fulfill that request. The server never relies on information from previous requests. If that information was important, the client would have sent it again in this request.

#### Application State vs Resource State
Please do not confuse between application state and resource state. Both are completely different things.

* **Application state** 
  * **server-side data** which servers store to identify incoming client requests, their previous interaction details, and current context information.

* **Resource state** 
  * **the current state of a resource on a server at any point of time** 
  * **has nothing to do with the interaction between client and server**. 
  * **What you get as a response from the server as API response. You refer to it as resource representation.**

**REST statelessness** means being free **on application state.**

<!-- https://restfulapi.net/statelessness/ -->


#### Advantages of Statelessness
There are some very noticeable advantages for having REST APIs stateless.

1. Statelessness helps in **scaling the APIs to millions of concurrent users by deploying it to multiple servers**. Any server can handle any request because there is **no session related dependency**.

2. Being stateless makes **REST APIs less complex** – **by removing all server-side state synchronization logic**.

3. A stateless API is also **easy to cache as well**. Specific software can decide whether or not to cache the result of an HTTP request just by looking at that one request. There’s no nagging uncertainty that state from a previous request might affect the cacheability of this one. It improves the performance of applications.

4. **The server never loses track of “where” each client is in the application because the client sends all necessary information with each request.**