# 📚 BookStore API

A modern RESTful API for an online bookstore built with **FastAPI**, **PostgreSQL**, **SQLAlchemy 2.0**, and **Docker**. The project provides authentication, book management, ordering, wishlists, and reviews while following a clean architecture suitable for learning and portfolio purposes.

## ✨ Features

* 🔐 JWT Authentication
* 👤 User registration and login
* 👑 Role-based authorization (Admin/User)
* 📖 CRUD operations for books
* ✍️ Author management
* 🛒 Book ordering
* ❤️ Wishlist management
* ⭐ Book reviews and ratings
* 🗄️ PostgreSQL database
* 🔄 Alembic database migrations
* 🐳 Docker & Docker Compose support
* 🧪 API testing with Pytest
* 📄 Automatic API documentation (Swagger/OpenAPI)

## 🛠️ Tech Stack

* FastAPI
* SQLAlchemy 2.0 (Async)
* PostgreSQL
* Alembic
* AsyncPG
* Pydantic
* JWT Authentication
* Docker
* Pytest

## 📂 Project Structure

```
.
├── .github/
├── .vscode/
├── alembic/
├── app/
│   ├── routers/
│   ├── models.py
│   ├── schemas.py
│   ├── crud.py
│   ├── database.py
│   ├── auth.py
│   ├── config.py
│   └── main.py
├── tests/
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── alembic.ini
├── bookstore_schema.sql
├── clean_db.py
└── README.md
```

## 🚀 Getting Started

### Clone the repository

```bash
git clone https://github.com/yourusername/bookstore-api.git
cd bookstore-api
```

### Configure environment

Create a `.env` file:

```env
DATABASE_URL=postgresql+asyncpg://postgres:postgres@db:5432/bookstore
SECRET_KEY=your_secret_key
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30
```

### Start the application

```bash
docker compose up --build
```

### Run database migrations

```bash
docker compose exec web alembic upgrade head
```

### API Documentation

Swagger UI:

```
http://localhost:8000/docs
```

ReDoc:

```
http://localhost:8000/redoc
```

## 🧪 Running Tests

```bash
pytest
```

## 📌 Main API Endpoints

### Authentication

* `POST /auth/register`
* `POST /auth/login`

### Books

* `GET /books`
* `GET /books/{id}`
* `POST /books`
* `PUT /books/{id}`
* `DELETE /books/{id}`

### Authors

* `GET /authors`
* `POST /authors`

### Orders

* `POST /orders`
* `GET /orders`

### Wishlist

* `POST /wishlist/{book_id}`
* `GET /wishlist`
* `DELETE /wishlist/{book_id}`

### Reviews

* `POST /reviews/{book_id}`
* `GET /reviews/{book_id}`

## 🔒 Authorization

The API uses **JWT Bearer Authentication**.

Some endpoints require **Admin** privileges, while others are available to authenticated users only.


## 📄 License

This project is under MIT license.

## Author
That project was made by **drizzy1772**
