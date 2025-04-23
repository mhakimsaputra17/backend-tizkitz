# Movie Ticket Booking API

A RESTful API built with Gin framework for a movie ticket booking system.

## Features

- API versioning
- Authentication and authorization
- User profile management
- Movie listings (upcoming, popular)
- Scheduling and seat reservation
- Order management
- Admin panel for movie management

## Prerequisites

- Go 1.16 or higher
- [Gin framework](https://github.com/gin-gonic/gin)
- [Air](https://github.com/air-verse/air) for hot reload during development

## Installation

1. Clone the repository

```bash
git clone <your-repo-url>
cd routing_gin
```

2. Install dependencies

```bash
go mod init routing_gin
go get -u github.com/gin-gonic/gin
```

3. Install Air globally (if not already installed)

```bash
go install github.com/air-verse/air@latest
```

## Project Structure

```
routing_gin/
├── main.go      # Entry point with route definitions
└── README.md    # Documentation
```

## Development

### Run with Air for hot reload

```bash
air
```

Air will watch for file changes and automatically rebuild and restart your application.

## API Endpoints

### Public Routes

- `GET /api/v1/movies` - List all movies with filters
- `GET /api/v1/movies/upcoming` - Get upcoming movies
- `GET /api/v1/movies/popular` - Get popular movies
- `GET /api/v1/movies/:id` - Get movie details
- `GET /api/v1/schedules` - Get movie schedules
- `GET /api/v1/schedules/:id/seats` - Get available seats

### Authentication Routes

- `POST /api/v1/auth/register` - Register new user
- `POST /api/v1/auth/login` - Login

### User Routes (Authenticated)

- `GET /api/v1/user/profile` - Get user profile
- `PUT /api/v1/user/profile` - Update user profile
- `POST /api/v1/user/orders` - Create new order
- `GET /api/v1/user/orders` - Get order history

### Admin Routes

- `GET /api/v1/admin/movies` - Get all movies (admin view)
- `POST /api/v1/admin/movies` - Create new movie
- `PUT /api/v1/admin/movies/:id` - Update movie
- `DELETE /api/v1/admin/movies/:id` - Delete movie
