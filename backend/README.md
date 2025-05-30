# Restaurant Management System - Backend

Laravel backend for the Restaurant Management System with API endpoints and admin panel.

## Features

- Laravel 10.x framework
- Laravel Breeze authentication
- PostgreSQL database integration
- RESTful API endpoints
- Docker containerization

## Requirements

- PHP >= 8.2
- Composer
- PostgreSQL
- Docker (optional)

## Local Development Setup

1. Install dependencies:
```bash
composer install
```

2. Copy environment file:
```bash
cp .env.example .env
```

3. Generate application key:
```bash
php artisan key:generate
```

4. Configure database in .env:
```env
DB_CONNECTION=pgsql
DB_HOST=database
DB_PORT=5432
DB_DATABASE=restaurant_db
DB_USERNAME=postgres
DB_PASSWORD=secret
```

5. Run migrations:
```bash
php artisan migrate
```

6. Start development server:
```bash
php artisan serve
```

## Docker Setup

The application can be run in a Docker container using the provided Dockerfile and docker-compose.yml in the root directory.

```bash
docker-compose up -d
```

## API Documentation

API endpoints will be documented here as they are implemented.

### Authentication

- POST /api/register - Register new user
- POST /api/login - User login
- POST /api/logout - User logout

### Restaurants

- GET /api/restaurants - List all restaurants
- GET /api/restaurants/{id} - Get restaurant details
- POST /api/restaurants - Create new restaurant (admin)
- PUT /api/restaurants/{id} - Update restaurant (admin)
- DELETE /api/restaurants/{id} - Delete restaurant (admin)

### Menu Items

- GET /api/restaurants/{id}/menu - Get restaurant menu
- POST /api/restaurants/{id}/menu - Add menu item (admin)
- PUT /api/restaurants/{id}/menu/{itemId} - Update menu item (admin)
- DELETE /api/restaurants/{id}/menu/{itemId} - Delete menu item (admin)

### Orders

- GET /api/orders - List user orders
- POST /api/orders - Create new order
- GET /api/orders/{id} - Get order details

## Testing

Run the test suite:

```bash
php artisan test
```

## Directory Structure

```
├── app/                 # Application core code
│   ├── Http/           # Controllers, Middleware
│   ├── Models/         # Eloquent models
│   └── Services/       # Business logic
├── config/             # Configuration files
├── database/           # Migrations and seeders
├── routes/             # API and web routes
├── tests/              # Test cases
└── storage/            # Logs, cache, uploads
```

## Contributing

1. Create a new branch
2. Make your changes
3. Run tests
4. Submit a pull request

## License

MIT