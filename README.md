# E-Ticket — Web-Based Event Reservation and Ticket Management System

WMA4 · Tarlac State University, College of Computer Studies · Group 2

E-Ticket lets attendees browse events, reserve tickets (one e-ticket with a QR code per attendee) and
lets administrators confirm reservations, record payments, validate tickets at the door and view reports.

## Repository structure

| Folder | Contents |
| ------ | -------- |
| [`frontend/`](frontend) | Bootstrap 5 + JavaScript UI (login, attendee and admin screens). See its [README](frontend/README.md). |
| [`backend/`](backend) | Laravel 12 REST API + MySQL (models, migrations, seeders). See its [README](backend/README.md). |

## Quick start

```bash
cd backend
composer install
cp .env.example .env
php artisan key:generate
# create the "eticket" database, then:
php artisan migrate:fresh --seed

cd ..
php -S localhost:8000 -t frontend backend/router.php
```

Open <http://localhost:8000>. Full setup details are in [`backend/README.md`](backend/README.md).

## Demo accounts (development only)

| Role          | Email                 | Password    |
| ------------- | --------------------- | ----------- |
| Administrator | admin@eticket.test    | admin123    |
| Attendee      | attendee@eticket.test | attendee123 |

## Branching

`main` holds the combined project. Work on a feature branch and open a pull request into `main`.
