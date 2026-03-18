# 💳 Fraud Detection Payment System

A backend payment processing system built using **Spring Boot** that simulates real-world fintech workflows and detects fraudulent transactions based on predefined rules.

---

## 🚀 Features

- ✅ Create Payment API  
- ✅ Retrieve User Transactions  
- ✅ Fraud Detection System:
  - High-value transactions (> 50,000)
  - Rapid repeated transactions  
- ✅ MySQL Database Integration  
- ✅ RESTful API Design  

---

## 🛠️ Tech Stack

- Java  
- Spring Boot  
- REST APIs  
- MySQL  
- Gradle  

---

## 📌 API Endpoints

### 🔹 1. Create Payment

**POST** `/payments`

#### Request Body:
```json
{
  "userName": "Dharunika",
  "amount": 1000
}
Response:
{
  "id": 1,
  "userName": "Dharunika",
  "amount": 1000,
  "status": "SUCCESS"
}
🔹 2. Get User Transactions

GET /payments/{userName}

Example:
GET /payments/Dharunika
⚠️ Fraud Detection Rules

🚨 Transactions above 50,000 → flagged as FRAUD_HIGH_AMOUNT

🚨 Multiple rapid requests → flagged as FRAUD_TOO_MANY_REQUESTS

⚙️ Setup Instructions
1️⃣ Clone the repository
git clone https://github.com/DharunikaHari-98/fraud-payment-system.git
cd fraud-payment-system
2️⃣ Configure MySQL

Create database:

CREATE DATABASE payment_db;

Update application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/payment_db
spring.datasource.username=root
spring.datasource.password=yourpassword
3️⃣ Run the application
./gradlew bootRun

Or run Application.java from IDE.

🧪 Testing

Use Postman or any API client:

POST /payments

GET /payments/{userName}

📊 Project Highlights

Designed modular backend architecture

Implemented real-world fraud detection logic

Built scalable REST APIs

Integrated persistent storage using MySQL


⭐ Future Improvements

Add authentication (JWT)

Machine learning-based fraud detection

Docker deployment
