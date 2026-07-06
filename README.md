# BookStore API

Production-ready REST API for an online bookstore with authentication, book management, wishlists, reviews, and order processing.

## Stack

* FastAPI
* PostgreSQL
* SQLAlchemy 2.0 (Async)
* Alembic
* JWT Authentication
* Docker Compose
* Pytest

## Key Features

* ✅ JWT authentication
* ✅ User registration and login
* ✅ Role-based authorization (Admin/User)
* ✅ CRUD operations for books
* ✅ Author management
* ✅ Order management
* ✅ Wishlist support
* ✅ Book reviews and ratings
* ✅ Async SQLAlchemy 2.0
* ✅ PostgreSQL database
* ✅ Alembic database migrations
* ✅ Docker Compose support
* ✅ Test coverage with Pytest

## API Scheme

<img width="1445" height="970" alt="tonka5bookapishka" src="https://github.com/user-attachments/assets/eb0118a8-e830-4e63-97b6-a262b0420332" />


## API Endpoints

| Method | Path                  | Description                 |
| ------ | --------------------- | --------------------------- |
| POST   | `/auth/register`      | Register new user           |
| POST   | `/auth/login`         | Login and receive JWT token |
| GET    | `/books`              | Get all books               |
| GET    | `/books/{id}`         | Get book by ID              |
| POST   | `/books`              | Create book (Admin)         |
| PUT    | `/books/{id}`         | Update book (Admin)         |
| DELETE | `/books/{id}`         | Delete book (Admin)         |
| GET    | `/authors`            | Get all authors             |
| POST   | `/authors`            | Create author (Admin)       |
| POST   | `/orders`             | Create order                |
| GET    | `/orders`             | Get user orders             |
| POST   | `/wishlist/{book_id}` | Add book to wishlist        |
| GET    | `/wishlist`           | Get wishlist                |
| DELETE | `/wishlist/{book_id}` | Remove book from wishlist   |
| POST   | `/reviews/{book_id}`  | Create review               |
| GET    | `/reviews/{book_id}`  | Get book reviews            |

## Quick Start

```bash
git clone https://github.com/yourusername/bookstore-api.git
cd bookstore-api

docker compose up --build

docker compose exec web alembic upgrade head
```

## Structure of Project

```
bookstore-api
│
├── app/
│   ├── routers/
│   ├── auth.py
│   ├── config.py
│   ├── crud.py
│   ├── database.py
│   ├── models.py
│   ├── schemas.py
│   └── main.py
│
├── alembic/
├── tests/
├── docker-compose.yml
├── Dockerfile
├── requirements.txt
├── alembic.ini
└── README.md
```

## API Docs

Swagger UI available at:

```
http://localhost:8000/docs
```

### Swagger UI Image

<img width="1364" height="1497" alt="Screenshot 2026-06-26 at 17-18-39 BookStoreApishka - Swagger UI" src="https://github.com/user-attachments/assets/825b0704-b160-490b-be47-7c50a2e39a19" />


### Live API

https://bookapishka.onrender.com

## Author

This project is developed by **Drizzy1772**.

## License

This project is licensed under the MIT License.
