# 🎬 Movie Ticket Booking System

A **Microservices-based Movie Ticket Booking System** built using **Java, Maven, MySQL, and MongoDB**. This project simulates an online movie ticket booking platform where users can browse movies, search showtimes, book seats, make payments, and receive booking notifications.

---

## 📌 Features

* 👤 User Registration & Authentication
* 🎥 Movie and Event Management
* 🔍 Search Movies & Showtimes
* 🎟️ Seat Booking System
* 💳 Payment Processing
* 📩 Booking Notifications
* 🗄️ MySQL & MongoDB Integration
* ⚡ RESTful APIs using Java HTTP Server
* 🏗️ Microservices Architecture

---

## 🛠️ Tech Stack

### Backend

* Java 17+
* Maven
* REST APIs
* Java HttpServer (`com.sun.net.httpserver.HttpServer`)

### Databases

* MySQL
* MongoDB

### Libraries

* Gson
* MySQL Connector/J

### Tools

* Git
* GitHub
* IntelliJ IDEA / Eclipse / VS Code
* Postman (API Testing)

---

## 📂 Project Structure

```text
Movie-Ticket-Booking/
│
├── booking-service/
├── event-service/
├── notification-service/
├── payment-service/
├── search-service/
├── user-service/
│
├── .gitignore
└── README.md
```

---

# ⚙️ Prerequisites

Before running the project, install:

* Java 17 or above
* Apache Maven
* MySQL Server
* MongoDB
* Git

---

# 🔧 Configuration

Update the MySQL password in each service where applicable.

Example:

```properties
db.username=root
db.password=YOUR_PASSWORD
```

> **Note:** MongoDB configuration does not require any changes unless your local setup differs.

---

# 🚀 Build the Services

Each service is an independent Maven project.

Navigate into a service directory and run:

```bash
mvn clean package
```

This downloads all dependencies and creates the executable JAR inside the `target/` directory.

---

# ▶️ Run the Services

Open a separate terminal for each service.

## 1. User Service (Port 8081)

```bash
cd user-service
java -cp "target/user-service-1.0-SNAPSHOT.jar;lib/*" user.Main
```

---

## 2. Event Service (Port 8082)

```bash
cd event-service
java -cp "target/event-service-1.0-SNAPSHOT.jar;lib/*" event.Main
```

---

## 3. Booking Service (Port 8084)

```bash
cd booking-service
java -cp "target/booking-service-1.0-SNAPSHOT.jar;lib/*" booking.Main
```

---

## 4. Payment Service (Port 8085)

```bash
cd payment-service
java -cp "target/payment-service-1.0-SNAPSHOT.jar;lib/*" payment.Main
```

---

## 5. Search Service (Port 8083)

```bash
cd search-service
java -cp "target/search-service-1.0-SNAPSHOT.jar;lib/*" search.Main
```

---

## 6. Notification Service (Port 8086)

```bash
cd notification-service
java -cp "target/notification-service-1.0-SNAPSHOT.jar;lib/*" notification.Main
```

---

# 🧪 API Verification

Once all services are running, test the APIs using Postman or cURL.

| Service      | Endpoint                                                 |
| ------------ | -------------------------------------------------------- |
| User         | `POST http://localhost:8081/api/auth/login`              |
| Event        | `GET http://localhost:8082/api/events/movies`            |
| Search       | `GET http://localhost:8083/search/showtimes?movieId=...` |
| Booking      | `GET http://localhost:8084/showtimes/{id}/seats`         |
| Payment      | `POST http://localhost:8085/payments`                    |
| Notification | `POST http://localhost:8086/notifications`               |

---

# 🗃️ Database

### MySQL

Used by:

* User Service
* Event Service
* Booking Service
* Payment Service

Update the database credentials in the corresponding `config.properties` file.

### MongoDB

Used for storing search-related or document-based data.

No configuration changes are required for a default local installation.

---

# 📷 Screenshots

You can add screenshots of:

* Home Page
* User Login
* Movie Listing
* Seat Selection
* Payment Page
* Booking Confirmation
* API Testing (Postman)

---

# 📌 Future Improvements

* JWT Authentication
* API Gateway
* Service Discovery
* Docker Support
* Kubernetes Deployment
* Email & SMS Notifications
* Admin Dashboard
* Online Payment Gateway Integration

---

# 👨‍💻 Authors

Developed as an academic project using a microservices architecture to demonstrate distributed application development with Java and Maven.

---

# 📄 License

This project is intended for educational and learning purposes.
