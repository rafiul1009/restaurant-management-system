# Restaurant Management System

A full-stack restaurant management system built with Laravel, React, and PostgreSQL, all containerized with Docker.

## Features

### Backend (Laravel)
- Admin panel with Laravel Breeze authentication
- RESTful API endpoints for frontend integration
- PostgreSQL database integration
- Docker containerization

### Frontend (React + Vite)
- Modern UI for restaurant and menu browsing
- Shopping cart functionality
- Order placement system
- TypeScript integration

## Prerequisites

- Docker and Docker Compose
- Node.js (for local development)
- Composer (for local development)

## Project Structure

```
├── frontend/             # React.js frontend application
│   ├── Dockerfile       # Frontend container configuration
│   └── src/             # React source code
├── backend/             # Laravel backend application
│   ├── Dockerfile      # Backend container configuration
│   └── src/            # Laravel source code
└── docker-compose.yml  # Docker services configuration
```

## Getting Started

1. Clone the repository:
```bash
git clone <repository-url>
cd restaurant-management-system
```

2. Start the Docker containers:
```bash
docker-compose up -d
```

3. The services will be available at:
- Frontend: http://localhost:3000
- Backend: http://localhost:8000
- Database: localhost:5432

## Development

### Frontend Development
```bash
cd frontend
npm install
npm run dev
```

### Backend Development
```bash
cd backend
composer install
php artisan serve
```

## Environment Variables

### Backend (.env)
```
DB_CONNECTION=pgsql
DB_HOST=database
DB_PORT=5432
DB_DATABASE=restaurant_db
DB_USERNAME=postgres
DB_PASSWORD=secret
```

## License

MIT