Microservices Using ASP.NET Core
-------------

The term microservices portrays a software development style that has
grown from contemporary trends to set up practices that are meant to
increase the speed and efficiency of developing and managing software
solutions at scale. Microservices is more about applying a certain
number of principles and architectural patterns as architecture. Each
microservice lives independently, but on the other hand, also all rely
on each other. All microservices in a project get deployed in production
at their own pace, on-premise on the cloud, independently, living side
by side.

Microservices Architecture
--------------------------

The following picture from [Microsoft
Docs](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/microservices)
shows the microservices architecture style.

![Microservice Using ASP.NET
Core](https://csharpcorner-mindcrackerinc.netdna-ssl.com/article/microservice-using-asp-net-core/Images/Microservice%20Using%20ASP.NET%20Core.png) 

There are various components in a microservices architecture apart from
microservices themselves.

**Management**. Maintains the nodes for the service.

**Identity Provider**. Manages the identity information and provides
authentication services within a distributed network.

**Service Discovery**. Keeps track of services and service addresses and
endpoints.

**API Gateway**. Serves as client’s entry point. Single point of contact
from the client which in turn returns responses from underlying
microservices and sometimes an aggregated response from multiple
underlying microservices.

**CDN**. A content delivery network to serve static resources for e.g.
pages and web content in a distributed network

**Static Content** The static resources like pages and web content

Microservices are deployed independently with their own database per
service so the underlying microservices look as shown in the following
picture.

![Microservice Using ASP.NET
Core](https://www.codeproject.com/KB/aspnet/1276639/image002.png) 

 

Monolithic vs Microservices Architecture
----------------------------------------

Monolithic applications are more of a single complete package having all
the related needed components and services encapsulated in one package.

Following is the diagrammatic representation of monolithic architecture
being package completely or being service based.

![Microservice Using ASP.NET
Core](https://www.codeproject.com/KB/aspnet/1276639/image003.png) 

Microservice is an approach to create small services each running in
their own space and can communicate via messaging. These are independent
services directly calling their own database.

Following is the diagrammatic representation of microservices
architecture.

![Microservice Using ASP.NET
Core](https://www.codeproject.com/KB/aspnet/1276639/image004.png) 

In monolithic architecture, the database remains the same for all the
functionalities even if an approach of service-oriented architecture is
followed, whereas in microservices each service will have its own
database.

Docker Containers and Docker installation
-----------------------------------------

Containers like Dockers and others slice the operating system resources,
for e.g. the network stack, processes namespace, file system hierarchy
and the storage stack. Dockers are more like virtualizing the operating
system. Learn more about dockers
[here](https://www.docker.com/resources/what-container). Open
[this](https://docs.docker.com/docker-for-windows/install/) URL and
click on Download from Docker hub. Once downloaded, login to the Docker
and follow instructions to install Docker for Windows.

Microservice using ASP.NET Core
-------------------------------

This section will demonstrate how to create a Product microservice using
ASP.NET Core step by step with the help of pictures. The service would
be built using ASP.NET Core 2.1 and Visual Studio 2017. Asp.NET Core
comes integrated with VS 2017. This service will have its own DBcontext
and database with the isolated repository so that the service could be
deployed independently.

![Microservice Using ASP.NET
Core](https://www.codeproject.com/KB/aspnet/1276639/image005.png) 


https://www.codeproject.com/Articles/1276639/Microservice-using-ASP-NET-Core
