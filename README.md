# DKHTodo Project

This project is a full-stack task management application built with a Django backend and an Ember.js frontend. It allows users to create, manage, and organize tasks efficiently.

## Prerequisites

Ensure you have the following installed on your system:
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- [Node.js](https://nodejs.org/)
- [Yarn](https://yarnpkg.com/)
- [Python](htts://python.org)

## Setup Instructions

### 1. Clone the Repository
```bash
git clone <repository-url>
cd my-todo
```

### 2. Configure Environment Variables
## Environment Variables

Create a `.env` file in the root directory and add the following environment variables:
```bash
SECRET_KEY=your_secret_key
DB_NAME=postgres
DB_USER=dkhtodo
DB_PASS=dkhtodo
DB_HOST=postgres
DB_PORT=5432
API_URL=http://localhost:8000
API_USERNAME=dkhtodo
API_PASSWORD=dkhtodo
```
### 3. Start the applicatino
`docker compose up --build -d`

### 4. Initialize the backend
```bash
docker compose exec -ti api sh -c 'python manage.py makemigrations'
docker compose exec -ti api sh -c 'python manage.py migrate'
docker compose exec -ti api sh -c 'python manage.py createsuperuser --username=${API_USERNAME:-dkhtodo} --email=dkhtodo@passiveobserver.com'
```
### 5. Access the Application
* Frontend: http://localhost:4200
* backend: http://localhost:8000

# Development
## Backend
`cd dkhtodo-backend`
`python manage.py runserver`

## Frontend
`cd dkhtodo-frontend`
`yarn start`

