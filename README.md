# EventRide-System-Kafka
A real-time rider tracking system built using Node.js and Kafka that streams rider location updates between producer and consumer services. It demonstrates event-driven architecture, message brokering, and scalable data processing using Apache Kafka for efficient distributed communication.


🚀 EventRide System (Kafka-Based Rider Tracking System)

A real-time event-driven backend system built using **Node.js** and **Apache Kafka** to simulate live rider location updates between services.

This project demonstrates how distributed systems communicate using a **publish-subscribe architecture**.

---

## 📌 Project Overview

In this system:

- A **Producer** sends rider location updates
- Kafka acts as a **message broker**
- A **Consumer** receives and processes those updates
- An **Admin service** creates and manages Kafka topics

This mimics real-world systems like:
- Uber / Ola ride tracking
- Delivery tracking systems (Swiggy, Zomato, Amazon)

---

## ⚙️ Tech Stack

- Node.js
- KafkaJS (Kafka client for Node.js)
- Apache Kafka
- JavaScript (ES6)

---

## 🧠 Architecture


Producer ---> Kafka Topic ---> Consumer
(Rider data) (rider-update) (Processes data)

Admin Service → Creates & manages Kafka topics


---

## 📂 Project Structure

```

kafka-app/
│
├── client.js        # Kafka connection setup
├── admin.js         # Creates Kafka topics
├── producer.js      # Sends rider updates
├── consumer.js      # Receives rider updates
├── package.json
└── README.md

🚀 How It Works
1. Admin Service
Connects to Kafka
Creates topic: rider-update
Defines number of partitions
2. Producer
Takes input from user (rider name, location)
Sends data to Kafka topic
Example input:

Tony, Bangalore

3. Kafka Broker
Stores and routes messages
Handles partitioning
4. Consumer
Listens to rider-update topic
Prints real-time updates
