# Spring Boot Basic Microservice Project

## Overview
This project demonstrates the use of microservices architecture using Spring Boot 3. It consists of three main services: 
1. **Eureka Naming Server** 
2. **Forex Service** 
3. **Currency Conversion Service**

Each microservice communicates via REST APIs, and the Eureka Naming Server facilitates service discovery.

## Prerequisites
- Java 17+
- Maven 3.8+
- Spring Boot 3.x   

## Services Overview
### 1. Eureka Naming Server
This service acts as a registry where all other microservices register themselves. It also enables the discovery of other services.

### 2. Forex Service
This service provides currency exchange rates. It has the following API:

- **GET** `/forex/from/{from}/to/{to}`: Fetches the exchange rate from one currency to another.

### 3. Currency Conversion Service
This service uses the Forex Service to convert amounts from one currency to another. It has the following API:

- **GET** `/currency-conversion/from/{from}/to/{to}/quantity/{quantity}`: Converts a given amount from one currency to another.

## Running the Application

1. **Clone the repository**:
    ```bash
    git clone https://github.com/your-repo/g-boot-basic-microservice.git
    cd g-boot-basic-microservice
    ```

2. **Run the Eureka Naming Server**:
    ```bash
    cd spring-boot-microservice-eureka-naming-server
    mvn spring-boot:run
    ```

3. **Run the Forex Service**:
    ```bash
    cd ../spring-boot-microservice-forex-service
    mvn spring-boot:run
    ```

4. **Run the Currency Conversion Service**:
    ```bash
    cd ../spring-boot-microservice-currency-conversion-service
    mvn spring-boot:run
    ```

## API Endpoints

### Forex Service
- **GET** `/forex/from/{from}/to/{to}`: Fetch the exchange rate from one currency to another. For example:
    ```
    GET http://localhost:8000/forex/from/USD/to/INR
    ```

### Currency Conversion Service
- **GET** `/currency-conversion/from/{from}/to/{to}/quantity/{quantity}`: Convert the given amount from one currency to another. For example:
    ```
    GET http://localhost:8100/currency-conversion/from/USD/to/INR/quantity/1000
    ```

## Authors and Contributions
This project was developed by the following contributors:

- [Maatangy](https://github.com/Maatangy/)
- [Bruhathi](https://github.com/bruhathisp) 





