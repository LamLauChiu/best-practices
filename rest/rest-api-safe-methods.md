# Safe Methods

* **An HTTP method is safe if it doesn't alter the state of the server.** In other words, a method is safe if it leads to a read-only operation. 

* **Several common HTTP methods are safe: GET, HEAD, or OPTIONS.** 
* **All safe methods are also idempotent, but not all idempotent methods are safe. For example, PUT and DELETE are both idempotent but unsafe.**

<!-- * As per HTTP specification, the GET and HEAD methods should be used only for retrieval of resource representations – and they do not update/delete the resource on the server. Both methods are said to be considered “safe“. -->

<!-- * This allows user agents to represent other methods, such as POST, PUT and DELETE, in a unique way so that the user is made aware of the fact that a possibly unsafe action is being requested – and they can update/delete the resource on server and so should be used carefully. -->

* Even if safe methods have a read-only semantic, servers can alter their state: e.g. they can log or keep statistics. What is important here is that by calling a safe method, the client doesn't request any server change itself, and therefore won't create an unnecessary load or burden for the server. 

* Browsers can call safe methods without fearing to cause any harm to the server; this allows them to perform activities like pre-fetching without risk. 

* Web crawlers also rely on calling safe methods.

<!-- https://developer.mozilla.org/en-US/docs/Glossary/Safe/HTTP -->