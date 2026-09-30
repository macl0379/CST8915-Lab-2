# CST8915-Lab-2

**Student Name**: Collin MacLeod
**Student ID**: macl0379
**Course**: CST8915 Full-stack Cloud-native Development
**Semester**: Fall 2026

---

## Demo Video

🎥 [Watch Demo Video](https://youtu.be/LTxfKaWh2L0)

---

## Reflection Question

### What changes did you make to the order-service and product-service to comply with the Configurations and Backing Services factors of the 12-Factor App methodology?

These services are compliant with the Configurations and Backing Services factors by making port values and backing service connection variables that are accessed in local `.env` files. Moving to a `.env` variables means that these services now follow the core of the the Configuration factor as it moves away from hard coded environment configurations. This allows the code better portability and security because the port you use will be kept hidden from public repositories and the services can be ran on any available port on a new server. Moving RabbitMQ to a remote  allows to be held unreachable URL and means that it can connect locally and a cloud database without the need to change any code.

### Why is it important to use environment variables instead of hard-coding configurations in your application?

It is important to use environment variables instead of hard-coding for multiple reasons. In a public repo setting, this might keep sensitive information private whe displaying work. When working on teams, this allows services to be ran on a variety of ports or credentials making it easy to run a given service on a new server.

### Why is it important to have separate repositories for each microservice? How does this help maintain independence and scalability of each service?

Keeping these microservices seperate allows for the code to scale easily and healthily. It puts up a wall between services to ensure that any errors in service A, will effect service B. When these services are run on different servers, this allows horizontal scaling by giving the ability to increase number of resources for any given link in the chain. If one services logic requires more work, you can easily scale at that instance without adding costs for other services.

## Associated Repositaries

- (Order Service)[https://github.com/macl0379/store-front]
- (Product Service)[https://github.com/macl0379/product-service]
- (Store front)[https://github.com/macl0379/store-front]