# Architectural Constraints
REST defines 6 architectural constraints which make any web service – a true RESTful API.

1. Uniform interface
2. Client–server
3. Stateless
4. Cacheable
5. Layered system
6. Code on demand (optional)



### 1. Uniform interface

> Once a developer becomes familiar with one of your APIs, he should be able to follow a similar approach for other APIs.

* A resource in the system should have only one logical URI

* Any single resource should not be too large and contain each and everything in its representation. 

* Resource should contain links ( **HATEOAS** ) pointing to relative URIs to fetch related information.

* Resource representations follows specific guidelines for naming conventions, link formats, or data format (XML or/and JSON)

* Consistent Approach with standard and common use case of HTTP method

### 2. Client–server

> Servers and clients may also be replaced and developed independently, as long as the interface between them is not altered.

* Client application and server application evolve separately without any dependency on each other

### 3. Stateless
> No client context shall be stored on the server between requests. The client is responsible for managing the state of the application.

* The server will not store anything about the latest HTTP request the client made.

* No client context shall be stored on the server between requests. 

* The client is responsible for managing the state of the application.

### 4. Cacheable

> Well-managed caching partially or completely eliminates some client-server interactions, further improving scalability and performance.

* Caching brings performance improvement for the client-side and better scope for scalability for a server because the load has reduced.

* Caching shall be applied to resources when applicable, and then these resources MUST declare themselves cacheable. 

* Caching can be implemented on the server or client-side.


### 5. Layered system

* REST allows you to use a layered system architecture where you deploy the APIs on server A, and store data on server B and authenticate requests in Server C, for example. 

### 6. Code on demand (optional)

* Sending the static representations of resources in the form of XML or JSON or other formalt like UI widget rendering code is permitted.


> All the above constraints help you build a truly RESTful API, and you should follow them. Still, at times, you may find yourself violating one or two constraints. Do not worry; you are still making a RESTful API – but not “truly RESTful.”