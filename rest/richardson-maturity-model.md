# Richardson Maturity Model

<!-- 
https://martinfowler.com/articles/richardsonMaturityModel.html#level0

https://damienfremont.com/2017/11/23/rest-api-maturity-levels-from-0-to-5/ -->


Leonard Richardson analyzed a hundred different web service designs and divided them into four categories based on how much they are REST compliant. This model of division of REST services to identify their maturity level – is called Richardson Maturity Model.

Richardson used three factors to decide the maturity of a service i.e. URI, HTTP Methods and HATEOAS (Hypermedia). The more a service employs these technologies – more mature it shall be considered.

The levels of maturity according to Richardson’s model
The levels of maturity according to Richardson’s model
In this analysis, Richardson described these maturity levels as below:

Level Zero
Level One
Level Two
Level Three
Richardson Maturity Model
Richardson Maturity Model

Level Zero
Level zero of maturity does not make use of any of URI, HTTP Methods, and HATEOAS capabilities.

These services have a single URI and use a single HTTP method (typically POST). For example, most Web Services (WS-*)-based services use a single URI to identify an endpoint, and HTTP POST to transfer SOAP-based payloads, effectively ignoring the rest of the HTTP verbs.

Similarly, XML-RPC based services send data as Plain Old XML (POX). These are the most primitive way of building SOA applications with a single POST method and using XML to communicate between services.


Level One
Level one of maturity makes use of URIs out of URI, HTTP Methods, and HATEOAS.

These services employ many URIs but only a single HTTP verb – generally HTTP POST. They give each resource in their universe a URI. A unique URI separately identifies one unique resource – and that makes them better than level zero.


Level Two
Level two of maturity makes use of URIs and HTTP out of URI, HTTP Methods, and HATEOAS.

Level two services host numerous URI-addressable resources. Such services support several of the HTTP verbs on each exposed resource – Create, Read, Update and Delete (CRUD) services. Here the state of resources, typically representing business entities, can be manipulated over the network.

Here service designer expects people to put some effort into mastering the APIs – generally by reading the supplied documentation.

Level 2 is the excellent use-case of REST principles, which advocate using different verbs based on the HTTP request methods, and the system can have multiple resources.


Level Three
Level three of maturity makes use of all three, i.e. URIs and HTTP and HATEOAS.

This level is the most mature level of Richardson’s model, which encourages easy discoverability. This level makes it easy for the responses to be self-explanatory by using HATEOAS.

The service leads consumers through a trail of resources, causing application state transitions as a result.