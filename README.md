# Dockerized Flask App with PostgreSQL & Redis

This project is a Flask web application that connects to PostgreSQL and Redis, running inside Docker containers using docker-compose.

## Features:

- Flask web app
- PostgreSQL database integration
- Redis caching
- Docker & docker-compose for easy setup
- **Visitor Tracking**: Stores visitor names and timestamps in PostgreSQL.
- **Wave Counter API**: A `/wave` endpoint to track user interactions.
- **Get Wave Count API**: A `/get_count` endpoint to retrieve wave counts.
- **Environment Variables Support**: Uses `.env` for flexible configuration.
- **Enhanced Logging**: Displays errors and status messages for debugging.

## Setup Instructions:

### Clone the Repository:
```bash
git clone https://github.com/Ahmedheggy/Flask_app_3.git
cd Flask_app_3
```

### Create a .env File:
Create a `.env` file in the project root with the following content:
```env
POSTGRES_USER=user
POSTGRES_PASSWORD=password
POSTGRES_DB=mydatabase
REDIS_HOST=redis
```

### Build & Start Containers:
```bash
docker-compose up --build -d
```

### Access the Web App:
Open in browser: [http://localhost:8000](http://localhost:8000)

### Check Database (Inside Container):
```bash
docker exec -it docker_task3-db-1 psql -U user -d mydatabase
```

### List Tables:
```sql
\dt
```

### Query Data:
```sql
SELECT * FROM visits;
```