# Kafka-Food-Ordering-System

## Overview
This project is a scalable, resilient, and decoupled food ordering system that leverages Kafka for asynchronous communication and enables real-time analytics. It consists of a frontend client, multiple backend services, and a Kafka message broker for efficient data distribution.

## Architecture
<img width="708" height="500" alt="Screenshot 2024-01-01 232829" src="https://github.com/Shreyas-028/Kafka-Food-Ordering-System/assets/79562771/c9b3724d-da76-4813-a99b-9a24b426e726">

## Key Components:

1. Food Ordering Client (Frontend):
    - User interface for placing orders.
    - Collects order details and communicates with backends via Kafka.
    
2. Orders Backend:
    - Manages order data and interacts with Kafka.
    
3. Transactions Backend:
    - Processes payment transactions.
    - Updates order status in the database.
    
4. Email Backend:
    - Sends order confirmation emails.
    
5. Analytics Backend:
    - Performs real-time analytics on order data.
   
6. Kafka:
    - Message broker for asynchronous communication.
    - Distributes order data to multiple backends.

## Project Flow

1. User initiates an order on the frontend.
2. Frontend sends order details to Kafka's order_details topic.
3. Kafka distributes order data to Transactions, Email, and Analytics Backends.
4. Transactions Backend processes payment and writes confirmation to order_confirmed topic.
5. Email and Analytics Backends read order_confirmed topic for verified orders.
6. Frontend reads order_confirmed topic for payment status and order details.
7. Frontend updates customer interface with order confirmation.

   

https://github.com/Shreyas-028/Kafka-Food-Ordering-System/assets/79562771/348e8e5d-8e26-4a4c-bfa5-aa22e7adbc66



## Key Features

- Scalability to handle high order volumes.
- Decoupled services for easier maintenance and updates.
- Resilience through Kafka's fault tolerance mechanisms.
- Real-time analytics for immediate insights into order trends, customer behavior, and inventory management.
- Asynchronous communication for improved responsiveness.
