Event Analytics API

Build your own Analytics API service using FastAPI and TimescaleDB (a time-series extension for PostgreSQL).
This project lets you create a time-series backend to ingest, store, and query analytics data — perfect for tracking web app events, traffic, metrics, and more.


🚀 Features

FastAPI backend — a super-fast API framework using async Python

Time-series database using TimescaleDB for efficient handling of large analytics datasets

Docker & Docker Compose support for easy development and deployment

Designed to be production-ready and extensible


📦 Tech Stack

| Component        | Technology               |
| ---------------- | ------------------------ |
| API Framework    | FastAPI                  |
| Database         | PostgreSQL + TimescaleDB |
| ORM              | SQLModel / SQLAlchemy    |
| Data validation  | Pydantic                 |
| Containerisation | Docker + Docker Compose  |


🧱 Getting Started

Prerequisites

Make sure you have the following installed:

Python 3.9+

Docker & Docker Compose

TimescaleDB (installed via Docker Compose below)

🐳 Using Docker (recommended)


1. Build the Docker image

```bash
docker build -t analytics-api -f Dockerfile.web 

```
2. Run using Docker Compose
```bash
docker compose up --watch

```
3. Stop and clean up

```bash
docker compose down

```

4. Open a shell inside the container

```bash 

docker compose run app /bin/bash

```

🛠 Development

After starting the project locally:

Modify or extend API routes in the src directory.

Use environment variables or .env files for database and service config.

Multi-container orchestration handled by Docker Compose.


📊 Usage

Once the API is up and running:

Send your analytics event data via HTTP endpoints.

Store this data in TimescaleDB hypertables.

Query aggregated analytics (e.g., time buckets, metrics trends) via API endpoints.

(Example API route details and request schemas should be added here if you extend this file.)


📦 Project Structure


```graphql 

├── src/                     # Main application code
├── Dockerfile.web           # Dockerfile for the web service
├── compose.yaml             # Docker Compose configuration
├── requirements.txt         # Python dependencies
├── .env.compose             # Environment variables config for Compose
├── README.md             
└── LICENSE      

```




