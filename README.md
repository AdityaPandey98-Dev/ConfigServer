# Spring Cloud Config Server

A production-ready **Spring Cloud Config Server** that centralizes configuration management for all Spring Boot microservices. Configuration properties are stored in a Git repository and served dynamically to client applications at startup.

This project is part of a complete Java Microservices ecosystem and integrates with **Eureka Server**, **Spring Boot Admin**, **Zipkin**, and **Spring Cloud Gateway**.

---

## Features

* Centralized configuration management
* Externalized configuration using Git
* Environment-specific configuration (Dev, QA, UAT, Prod)
* Spring Boot Actuator support
* Eureka Client integration
* Spring Boot Admin integration
* Version-controlled configuration
* Production-ready project structure

---

## Tech Stack

* Java 17
* Spring Boot
* Spring Cloud Config Server
* Spring Cloud
* Maven
* Git & GitHub
* Spring Boot Actuator
* Eureka Client
* Spring Boot Admin

---

## Project Structure

```text
ConfigServer
│── src
│   ├── main
│   │   ├── java
│   │   └── resources
│   │       └── application.properties
│   └── test
│
├── pom.xml
└── README.md
```

---

## Configuration Repository

The Config Server reads configuration files from a dedicated Git repository.

Example structure:

```text
ConfigRepository
│── application.properties
│── user-service.properties
│── product-service.properties
│── inventory-service.properties
│── order-service.properties
│── payment-service.properties
```

---

## Running the Config Server

### Clone the repository

```bash
git clone <your-config-server-repository-url>
```

### Build the project

```bash
mvn clean install
```

### Run the application

```bash
mvn spring-boot:run
```

The Config Server starts on:

```text
http://localhost:8888
```

---

## Example Endpoints

Retrieve common configuration:

```text
GET http://localhost:8888/application/default
```

Retrieve configuration for a specific service:

```text
GET http://localhost:8888/payment-service/default
```

Retrieve configuration for a specific profile:

```text
GET http://localhost:8888/payment-service/dev
```

---

## Integration

This Config Server is designed to work with:

* Eureka Server
* Spring Cloud Gateway
* Spring Boot Admin
* Zipkin
* User Service
* Product Service
* Inventory Service
* Order Service
* Payment Service
* Notification Service

---

## Benefits

* Centralized configuration management
* Simplified application maintenance
* Git-based version control
* Environment-specific configuration
* Reduced configuration duplication
* Easy rollback using Git history
* Better scalability for distributed systems

---

## Future Enhancements

* Spring Cloud Bus
* Dynamic configuration refresh
* Configuration encryption
* HashiCorp Vault integration
* Kubernetes ConfigMap support
* Docker support
* Kubernetes deployment

---

## Author

**Aditya Pandey**

Java Full Stack Developer | Spring Boot | Microservices | React | AWS
