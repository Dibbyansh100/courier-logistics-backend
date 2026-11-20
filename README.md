# 📦 Courier & Logistics Tracking System — Backend

A Java Spring Boot REST API for managing courier bookings, shipment tracking, delivery agents, warehouses, customers, and payment records.

## 🛠️ Technology Stack

- **Backend:** Java 21, Spring Boot 3.3.4
- **Database:** PostgreSQL
- **ORM:** Spring Data JPA, Hibernate
- **Security:** Spring Security, HTTP Basic Authentication, role-based authorization
- **Other:** REST APIs, Lombok, Docker

## ✨ Key Features

- Create and manage courier shipments.
- Automatically generate unique shipment tracking numbers.
- Calculate shipping charges using package weight and fragile-package surcharges.
- Assign available delivery agents to shipments.
- Manage warehouse and customer information.
- Retrieve shipment tracking history.
- View and update payment records.
- Search, filter, sort, and paginate shipments.
- Apply role-based API access for Admin, Customer, and Delivery Agent users.

## 🧩 Core Modules

| Module | Responsibility |
|---|---|
| Customer | Customer management |
| Shipment | Booking, tracking, assignment and pricing |
| Delivery Agent | Agent details and availability |
| Warehouse | Warehouse management |
| Package | Package information and categories |
| Tracking History | Shipment tracking records |
| Payment | Payment records and status |
| Authentication | Login and role-based access |

## 🔗 REST API Examples

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/login` | User login |
| POST | `/api/shipments` | Create shipment |
| GET | `/api/shipments` | List shipments |
| GET | `/api/shipments/tracking/{trackingNumber}` | Find shipment by tracking number |
| GET | `/api/shipments/paginated` | Paginated shipments |
| PUT | `/api/shipments/{shipmentId}/assign-agent/{agentId}` | Assign delivery agent |
| GET | `/api/tracking/shipment/{shipmentId}` | Get shipment history |
| GET | `/api/payments` | List payment records |
| GET | `/api/warehouses` | List warehouses |
| GET | `/api/agents` | List delivery agents |

Protected endpoints require appropriate authentication and authorization.

## 🧮 Shipment Pricing

The current service implementation calculates a base shipping amount of ₹50 per kilogram and adds a ₹100 surcharge when the package is marked fragile.

These rates are demonstration business rules defined in the backend service.

## 🚀 Run Locally

**Prerequisites:** Java 21, PostgreSQL, Git, and Maven.

1. Clone the backend repository:

   `git clone https://github.com/Dibbyansh100/courier-logistics-backend.git`

2. Open the project directory:

   `cd courier-logistics-backend`

3. Create a PostgreSQL database named `LogisticAndTrack_db`.

4. Configure the database connection and credentials through the environment variables supported by `application.properties`.

5. Start the application:

   `mvn spring-boot:run`

The API runs on port `8088` by default unless overridden with `PORT`.

## 🔐 Security

The project currently uses Spring Security with HTTP Basic Authentication and role-based endpoint restrictions.

The authentication and password-storage implementation should be strengthened before using this system with real user accounts.

## 💻 Frontend Repository

[React Frontend & Screenshots](https://github.com/Dibbyansh100/courier-logistics-frontend)

[Live Frontend Demo](https://courierlogistics.vercel.app/)

## 👨‍💻 Developer

Dibbyansh Pandey — Java Full Stack Developer
