# Mini-Project---Real-time-Data-Pipeline-for-Twitter-Streaming
# 📡 Real-time Twitter Data Pipeline Project

> An end-to-end real-time data pipeline that collects, processes, and stores Twitter streaming data using Kafka, Spark Structured Streaming, and PostgreSQL, fully containerized with Docker.

---

## 🚀 Project Architecture

[Tweepy Producer] ↓ (streaming tweets JSON) [Kafka Topic: twitter-stream] ↓ (real-time ingestion) [Spark Structured Streaming Consumer] ↓ (batch processing) [PostgreSQL Database: tweets table]


## 🛠️ Tech Stack

- **Kafka** - Real-time message broker
- **Zookeeper** - Kafka cluster management
- **Python (Tweepy)** - Twitter Streaming API Producer
- **Apache Spark Structured Streaming** - Real-time data processing
- **PostgreSQL** - Data sink (relational database)
- **Docker** - Containerization
- **Docker Compose** - Multi-service orchestration

---

## 📦 Project Structure

/producer ├── producer.py # Kafka Producer sending tweets └── Dockerfile # Docker image for producer /consumer ├── consumer.py # Spark Structured Streaming Consumer └── Dockerfile # Docker image for consumer /docker-compose.yml # Service orchestration /init.sql # PostgreSQL schema initialization /README.md # Project documentation

---

## ⚡ How to Run

1. **Clone the repository**
   ```bash
   git clone <your-repo-link>
   cd <repo-folder>
Start all services with Docker Compose

bash

docker-compose up --build
Verify containers
Kafka and Zookeeper are up
Producer is sending tweets to Kafka
Consumer is processing tweets and saving into PostgreSQL
Access Database

Host: localhost
Port: 5432
Database: twitterdb
Table: tweets
Username: postgres
Password: postgres

🎯 Future Improvements
Integrate Apache Airflow for orchestration
Push processed data to AWS S3 as a data lake
Set up Grafana dashboard to monitor streaming jobs
Implement Kafka Connect for direct sink to database


📚 References
Apache Kafka Documentation
Apache Spark Structured Streaming
Tweepy Documentation
Docker Compose

Developed with ❤️ by Jun
