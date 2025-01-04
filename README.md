# Little Lemon Restaurant API

## Project Description

This is the backend API for the Little Lemon restaurant, developed as part of the Meta Backend Developer Capstone project. The API provides functionality for menu management and table booking system.

## Project Structure

```
capstone/
├── workspace/           # Virtual environment
│   └── littlelemon/    # Django project root
│       ├── littlelemon/            # Project settings
│       └── littlelemonrestaurant/  # Main app
└── assets/             # Project assets
```

## Features

- Menu API with full CRUD operations
- Table Booking API with authentication
- User registration and authentication using Djoser
- MySQL database integration

## API Endpoints

- Menu Items:

  - GET /restaurant/menu/
  - POST /restaurant/menu/
  - GET /restaurant/menu/{id}
  - PUT /restaurant/menu/{id}
  - DELETE /restaurant/menu/{id}

- Table Booking:

  - GET /restaurant/booking/tables/
  - POST /restaurant/booking/tables/
  - GET /restaurant/booking/tables/{id}
  - PUT /restaurant/booking/tables/{id}
  - DELETE /restaurant/booking/tables/{id}

- Authentication:
  - POST /auth/token/login/
  - POST /auth/token/logout/
  - POST /auth/users/

## Technologies

- Django
- Django REST Framework
- MySQL
- Djoser for authentication

## Setup Instructions

1. Create and activate virtual environment:

```bash
python -m venv workspace
workspace\Scripts\activate  # On Windows
```

2. Install dependencies:

```bash
pip install django djangorestframework mysqlclient djoser
```

3. Configure MySQL database in settings.py

4. Apply the migrations:

```bash
python manage.py migrate
```

5. Run the development server:

```bash
python manage.py runserver
```

## Authentication

The API uses token authentication. To access protected endpoints:

1. Obtain token through /auth/token/login/
2. Include in requests header:

```
Authorization: Token <your-token>
```

## Testing

Run tests using:

```bash
python manage.py test
```
