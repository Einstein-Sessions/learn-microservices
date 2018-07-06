# Microservices Architecture

Table of contents
=================

<!--ts-->
   * [What is a Service](#what-is-a-service)
<!--te-->

## What is a Service?

* A _service_ is a piece of software which provides functionality to other pieces of software
within your system.
* It provides a _service_ to other pieces of software.
* The other pieces of software could be a website, a mobile app or a desktop app or another 
service which uses another service to carry out a particular type of functionality.
* A _service_ provides functionality to these applications.

<p align="center">
    <img src="https://user-images.githubusercontent.com/29547780/42199133-a38c5420-7e84-11e8-8d29-e365622d89c4.png">
</p>

* For example in the _Shopping Website_ context, when a user places an order on the website,
the website would talk to the _service_ and the _service_ carries out the _CRUD_ operations 
of orders from the database. So it provides `functionality` to the website application.
* The communication of these software components and a _service_ occur over a network using
some kind of communication protocol.
* E.g a mobile app might communicate to a service via the Internet.
* A system which uses a _service_ or multiple services in this fashion is known to have a 
`Service Oriented Architecture` which is normally abbreviated as `SOA`.
* The main idea behind `SOA` is, instead of using packet modules within each client application,
I instead use a `Service` to provide functionality to my client applications and this allows
me to have many client applications using the same functionality. Also in the future I can have
new or different clients connected to the same service, reusing that same functionality.
* In the future I can have newer or different types of clients connected to the same _service_
reusing that functionality.

<p align="center">
    <img src="https://user-images.githubusercontent.com/29547780/42292847-7a439a98-7fcd-11e8-902e-5f5c3749f3a1.png">
</p>

* As an architecture, _SOA_ has been successful as it allows us to scale up our software when
demand increases by enabling us to have a copy of service on multiple servers.
* When traffic comes in, a `load balancer` will redirect that request to a specific instance
of the service.
* We can have multiple instances of that service. So when the demand increases, we just have
to increase the number of instances of the service running across servers.