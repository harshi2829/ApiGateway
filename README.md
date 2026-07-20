# API Gateway

The single entry point for the Banking System project. All client requests go through here and get routed to the right service.

Without a gateway, the client would need to know the port of every service. With the gateway, everything goes through port 8080 and the routing happens automatically based on the URL path.

## Tech Stack

- Java 17
- Spring Boot 3
- Spring Cloud Gateway
- Spring Cloud Eureka Client

## Port

8080

## Routing

| Path | Routes to |
|---|---|
| /auth/** | Auth Service (8081) |
| /accounts/** | Account Service (8082) |
| /transactions/** | Transaction Service (8083) |

## How to Run (with Docker)

This service is part of a larger Docker setup. Clone the main repo and follow the instructions there:
https://github.com/harshi2829/Banking-microservices-docker

## How to Run (standalone)

./mvnw spring-boot:run

## Part of

Banking Microservices project: https://github.com/harshi2829/Banking-microservices-docker
