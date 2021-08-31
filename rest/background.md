# What is an Rest?

* **REST** stands for **RE**presentational **S**tate **T**ransfer. 

* REST is **architectural style for distributed hypermedia systems** 

* REST was first introduced by **Roy Fielding** in the year 2000.
(He is known for REST and Apache, contributes URI, HTTP, and HTML)

* REST uses **HTTP protocol** for data communication.

* REST uses **Text, JSON and XML** to communicate with client and server.

> RESTful Web Services are basically REST Architecture based Web Services.

> REST + Web Services = RESTFul Web Services

* REST owns **6 guiding constraints** which must be satisfied if an interface needs to be referred as **RESTful**.
 
### Guiding Principles of REST

1. **Client–server** 
<!-- – By separating the user interface concerns from the data storage concerns, we improve the portability of the user interface across multiple platforms and improve scalability by simplifying the server components. -->

2. **Stateless** 
<!-- – Each request from client to server must contain all of the information necessary to understand the request, and cannot take advantage of any stored context on the server. 
Session state is therefore kept entirely on the client. -->

3. **Cacheable** 
<!-- – Cache constraints require that the data within a response to a request be implicitly or explicitly labeled as cacheable or non-cacheable. If a response is cacheable, then a client cache is given the right to reuse that response data for later, equivalent requests. -->

4. **Uniform interface** 
<!-- – By applying the software engineering principle of generality to the component interface, the overall system architecture is simplified and the visibility of interactions is improved. In order to obtain a uniform interface, multiple architectural constraints are needed to guide the behavior of components. REST is defined by four interface constraints: identification of resources; manipulation of resources through representations; self-descriptive messages; and, hypermedia as the engine of application state. -->

5. **Layered system** 
<!-- – The layered system style allows an architecture to be composed of hierarchical layers by constraining component behavior such that each component cannot “see” beyond the immediate layer with which they are interacting. -->

6. **Code on demand (optional)** 
<!-- – REST allows client functionality to be extended by downloading and executing code in the form of applets or scripts. This simplifies clients by reducing the number of features required to be pre-implemented. -->


## Resource

* **The key abstraction of information in REST is a resource**. 

> The key abstraction of information in REST is a resource. **Any information that can be named can be a resource: a document or image, a temporal service (e.g. “today’s weather in Los Angeles”), a collection of other resources, a non-virtual object (e.g., a person), and so on.** In other words, any concept that might be the target of an author’s hypertext reference must fit within the definition of a resource. A resource is a conceptual mapping to a set of entities, not the entity that corresponds to the mapping at any particular point in time. ( Roy Fielding’s dissertation)

<!-- Any information that can be named can be a resource: a document or image, a temporal service, a collection of other resources, a non-virtual object (e.g. a person), and so on. -->

<!-- * REST uses a resource identifier to identify the particular resource involved in an interaction between components. -->

* The **state** of the resource **at any particular timestamp** is known as **resource representation**. 

* A **representation consists of data, metadata describing the data and hypermedia links** which can help the clients in transition to **the next desired state**.

* The **data format** of a representation is known as a **media type**. 

* The **media type** identifies a specification that **defines how a representation is to be processed**. 

* **A truly RESTful API looks like hypertext.** Every addressable unit of information carries an address, either explicitly (e.g., link and id attributes) or implicitly (e.g., derived from the media type definition and representation structure).



### Questions when we develop RESTfull APIs:

* When should URI path segments be named with plural nouns?
* Which request method should be used to update resource state?
* How do I map non-CRUD operations to my URIs?
* What is the appropriate HTTP response status code for a given scenario?
* How can I manage the versions of a resource’s state representation?
* How should I structure a hyperlink in JSON?
