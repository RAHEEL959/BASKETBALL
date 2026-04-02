# 🏀 Basketball Web

A full-stack basketball league web application with a static HTML/CSS frontend and a Laravel REST API backend.

---

## Project Structure

```
BASKETBALL WEB/
├── BASKETBALL/          # Frontend (HTML/CSS)
└── basketball-backend/  # Backend (Laravel 12 API)
```
  ![Screenshot](https://github.com/RAHEEL959/BASKETBALL/blob/main/Capture.PNG)
---

## Frontend — `BASKETBALL/`

A static multi-page website built with HTML and CSS.

### Pages

| File | Description |
|------|-------------|
| `index.html` | Home / landing page |
| `schedule.html` | Game schedule |
| `teams.html` | Teams listing |
| `players.html` | Players listing |
| `videos.html` | Video gallery |
| `photos.html` | Photo gallery |
| `contact.html` | Contact form |

### Features
- Fixed glassmorphism navbar with logo
- Full-viewport hero section with animated basketball icon
- Responsive card grid for teams and players
- Video hero with overlay gallery
- Animated contact form with icon inputs
- Gold (`#ffcc00`) accent color theme throughout

### Run
Just open `BASKETBALL/index.html` in any browser — no build step required.

---

## Backend — `basketball-backend/`

A REST API built with **Laravel 12** using Sanctum for authentication.

### Requirements
- PHP >= 8.2
- Composer
- MySQL

### Setup

```bash
cd basketball-backend

# Install dependencies
composer install

# Copy environment file
cp .env.example .env

# Generate app key
php artisan key:generate

# Configure your database in .env
DB_DATABASE=basketball_backend
DB_USERNAME=root
DB_PASSWORD=

# Run migrations
php artisan migrate

# Start the server
php artisan serve
```

### API Endpoints

Base URL: `http://localhost:8000/api`

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET/POST/PUT/DELETE | `/teams` | Teams CRUD |
| GET/POST/PUT/DELETE | `/players` | Players CRUD |
| GET/POST/PUT/DELETE | `/schedules` | Schedules CRUD |
| GET/POST/PUT/DELETE | `/photos` | Photos CRUD |
| GET/POST/PUT/DELETE | `/videos` | Videos CRUD |
| GET | `/contacts` | List contact submissions |
| POST | `/contacts` | Submit a contact message |

### Database Models

- `User` — Auth with admin flag (`is_admin`)
- `Team` — Basketball teams
- `Player` — Player profiles
- `Schedule` — Game schedule entries
- `Photo` — Photo gallery items
- `Video` — Video gallery items
- `Contact` — Contact form submissions

### Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Laravel 12 |
| Auth | Laravel Sanctum |
| Database | MySQL |
| Testing | PestPHP |
| Dev Tools | Laravel Breeze, Pint, Sail |

---

## License

MIT
