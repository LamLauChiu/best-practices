# What is an API?


> An API (the full form is **Application Programming Interface**) is **a contract** ( or **specification**) promised by the software which it will honor if other software wants to interact with it for performing business operations.

> **API allows two or more software applications to talk to each other through a well-defined computing interface.**

# API Example in Real Life

1. Mobile App
    * real-time data e.g. weather information, emails, game scores etc. displayed is fetched through the APIs deployed on the server.
2. Webesite
    * fetch the data usingAJAX, Web Sockets, etc. through an API.

# What is the purpose of an API
The software applications are developed in pieces. To avoid writing a piece of software multiple times in different places, it is written as a reusable component.

**The API helps in making the component standard, reusable, easily understood by the users, and abstract. The abstraction helps in exposing only minimum relevant information to other entities and protect the business logic to perform an action.**

Making reusable APIs not only benefits the users, but it also makes easy the developer’s life as well. **The defined scope of API helps in the designing, testing, building, managing, and versioning of the component.**



<!-- # How to use API
We are not required to know how an API works internally for serving a specific business goal or any task. All we will need to know is how to interact with the API.

For example, all airline ticket booking applications will use an API exposed by the airline company. Anytime a customer uses any such application and books a flight ticket, the application passes the passenger and flight booking information to the API.

The booking API will process the data and book the ticket for the customer and the application will get a successful response with booking details in return.

The booking applications do not know and need not know how the API works internally. All they are required to do is pass the booking information in a well-defined format to the API and wait for the response.

Similarly, any application/mobile app can use an API or expose an API to other software. -->

# How to develop an API
### API Specification
The very first thing is a standard, clean, well documented, and easy to use API specification.

* A very clear business operation it will perform
* The API URL or interface
* HTTP protocal and methods
* Request structure and individual fields
* Response structure and individual fields
* Valid values for fields in request, where it is applicable
* Any mechanism for filering and sorting the data
* Any authentication/authorization information
* The possible success and error codes
* And, any other relevant information it should


### API Security
The information is of the utmost importance in any application, especially the user’s nonpublic personal information (NPI data). To protect this information, **API must be secured from unauthorized access**.

**Only authorized users with secure credentials should be able to access the API**.

### Audit Logging
1.  A publicly exposed API will be used by thousands of users every day. To understand how the API is used or abused by its user, it is necessary to **log the critical information related to API usages**.

2.  **A proper monitoring system will trigger the alerts in case of somebody misuses the API interface or make an unauthorized entry into the application**.

### Performance
* Make it usable in the first place
* Don't block the users except certain cases e.g. transfer and bill payments


<!-- API performance is very essential to make it usable in the first place. No application would like to block its users while a request is being processed in the server. Only certain applications are expected to block where they perform operations in real-time. For example, money transfer and bill payments.

A poorly performing API will not be used by its consumers and thus will cause a loss to the business. -->