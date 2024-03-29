<ins>**Monolithic Architecture:**</ins>
* A monolithic architecture is a traditional approach to designing software where an entire application is built as a single, indivisible unit. In this architecture, all the different components of the application, such as the user interface, business logic, and data access layer, are tightly integrated and deployed together.
* This means that any changes or updates to the application require modifying and redeploying the entire monolith.
* Monolithic architectures are often characterized by their simplicity and ease of development, especially for small to medium-sized applications.
* However, they can become complex and difficult to maintain as the size and complexity of the application grow.

<ins>**Micro-Service Architecture:**</ins>
* In a microservices architecture, an application is built as a collection of small, independent services, each representing a specific business capability. These services are loosely coupled and communicate with each other over a network, often using lightweight protocols like HTTP or messaging queues.
* Each service is responsible for a single functionality or feature of the application and can be developed, deployed, and scaled independently.
* The Microservice architecture has a significant impact on the relationship between the application and the database.
* Instead of sharing a single database with other microservices, each microservice has its own database. It often results in duplication of some data, but having a database per microservice is essential if you want to benefit from this architecture, as it ensures loose coupling.

<ins>**Difference between Monolithic and Micro-Service Architecture:**</ins>

<ins>**Monolithic Architecture:**</ins>

* Single-tier architecture
* Deployed as a single unit
* Horizontal scaling can be challenging
* Development is simpler initially
* Limited technology choices
* Entire application may fail if a part fails
* Easier to maintain due to its simplicity
* Communication between components is faster

<ins>**Micro-Servivce Architecture:**</ins>

* Multi-tier architecture
* Individual services can be deployed independently
* Easier to scale horizontally
* Development is complex due to managing multiple services
* Freedom to choose the best technology for each service
* Requires more effort to manage multiple services
* Individual services can fail without affecting others
* Communication may be slower due to network calls
