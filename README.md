# 📚 registry-service

> **Eureka Service Registry for Quiz App (Microservice Architecture)**

---

## 🚀 Introduction

Welcome to the **Registry Service** for the Quiz App!  
This project is a central piece in the microservice architecture of the Quiz platform, providing a robust Eureka-based service registry. It enables seamless discovery and communication between distributed microservices, ensuring that your system is always scalable, resilient, and easy to manage.

---

## 🏗️ What is Eureka Service Registry?

[Eureka](https://github.com/Netflix/eureka) is a REST-based service used for locating services for the purpose of load balancing and failover of middle-tier servers. In a microservices environment, the registry-service acts as the **"phone book"** where all services register themselves and discover others dynamically.

---

## 🧩 Features

- 🔍 **Service Discovery:** Dynamically locate and communicate with other microservices.
- 📈 **Scalability:** Easily add or remove services without manual intervention.
- 🛡️ **Resilience:** Built-in health checks and failover support.
- 🌐 **Web Dashboard:** Visual interface to monitor all registered services.
- 🔄 **Self-Healing:** Automatically removes unhealthy services from the registry.

---

## 🗂️ Project Structure

```
registry-service/
├── src/
│   └── main/
│       ├── java/
│       └── resources/
│           └── application.properties
├── pom.xml
└── README.md
```

- **pom.xml:** Maven dependencies and project config.
- **application.properties:** Eureka server and Spring Boot settings.

---

## 🛠️ Getting Started

### 1️⃣ Prerequisites

- **Java 8+**
- **Maven**

### 2️⃣ Clone & Build

```bash
git clone https://github.com/kundan424/registry-service.git
cd registry-service
mvn clean package
```

### 3️⃣ Run the Eureka Server

```bash
mvn spring-boot:run
```

> By default, Eureka Dashboard will be available at [http://localhost:8761](http://localhost:8761)

---

## 🤝 How to Use

1. **Register Microservices:**  
   Configure each microservice with the Eureka server URL (usually in `application.properties`):

   ```properties
   eureka.client.service-url.defaultZone=http://localhost:8761/eureka/
   ```

2. **Monitor with Dashboard:**  
   Open [http://localhost:8761](http://localhost:8761) to view registered instances in real-time.

3. **Scale Confidently:**  
   Add or remove microservices without changing any discovery logic — Eureka handles it.

---

## 🧑‍💻 Example application.properties

```properties
server.port=8761
spring.application.name=registry-service
eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false
```

---

## 📝 Customization

- **Change Port:** Edit `server.port` in `application.properties`.
- **Secure Dashboard:** Integrate with Spring Security for production use.
- **Cluster Mode:** Eureka can run in peer-aware mode for high availability.

---

## 📚 Resources

- [Spring Cloud Netflix Eureka Documentation](https://cloud.spring.io/spring-cloud-netflix/reference/html/)
- [Microservices with Spring Boot and Spring Cloud](https://spring.io/guides/gs/service-registration-and-discovery/)

---

## 🙋 FAQ

**Q: Why do I need a service registry?**  
A: In microservices, hardcoding service URLs doesn't scale. Eureka allows services to register and discover each other dynamically.

**Q: Can I use this in production?**  
A: Yes, but consider enabling security and running Eureka in cluster mode for high availability.

---

## 🤗 Contributing

We welcome contributions!  
Feel free to fork this repo, create a branch, and submit a pull request.

---

## 📜 License

> This repository does not specify a license. Please contact the repository owner for more details or to discuss licensing.

---

## 📬 Contact

For questions, suggestions, or support, please open an [issue](https://github.com/kundan424/registry-service/issues) or reach out to [kundan424](https://github.com/kundan424).

---

⭐️ _If you found this project helpful, please star the repository!_