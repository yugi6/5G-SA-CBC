# 5GSACBC - 5G SA Cell Broadcast Center Function

This project implements the **5G Standalone (SA) Cell Broadcast Center Function (CBCF)** using **Spring Boot** and Java. It handles communication via the `Namf_Communication` service interface as per 3GPP 5G architecture standards.

## Features

- 📡 **Non-Ue Communication Support**:
  - `NonUeMessageTransfer`
  - `NonUeN2InfoSubscribe`
  - `NonUeN2InfoUnsubscribe`
- 📦 Spring Boot RESTful APIs
- 🧩 Java model classes representing N2 and AMF entities
- 🛠 Maven project with build and dependency management

## Project Structure

```
5GSACBC/
├── pom.xml                     # Maven configuration
├── src/
│   └── main/
│       ├── java/
│       │   └── com/ugandhar/sacbc/
│       │       ├── controller/         # REST API Controllers
│       │       ├── model/              # Java models (e.g., GNbId, Tai, N2InfoContent)
│       │       └── Application.java    # Main Spring Boot application
│       └── resources/
│           ├── application.yml         # App configuration
│           └── ...                     # Additional config files
├── target/                    # Compiled artifacts
└── README.md
```

## Prerequisites

- Java 17+
- Maven 3.8+
- IDE (e.g., IntelliJ, Eclipse)

## Build & Run

```bash
# Build the application
mvn clean install

# Run the application
mvn spring-boot:run
```

## NamfCommunicationController API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/cbc/non-ue-msg` | POST | Transfers message from CBCF to AMF |
| `/cbc/subscribe`       | POST | Subscribes to N2 information from AMF |
| `/cbc/unsubscribe/{id}`     | POST | Unsubscribes N2 info notifications |

## StubResponseController API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/namf-comm/v1/non-ue-msg` | POST | Transfers message from CBCF to AMF stub response |
| `/namf-comm/v1//non-ue-n2-info-subscribe`       | POST | Subscribes to N2 stub response  |
| `/namf-comm/v1//non-ue-n2-info-subscribe/{subscriptionId}`     | POST | Unsubscribes N2 stub response |

## Author

**Ugandhar Gunturu**

---

> This project is part of a 5G core network CBCF implementation.
