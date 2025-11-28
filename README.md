# ALX Travel App

A Django-based travel application with REST API and comprehensive documentation.

## Features

- Django 4.2+ with Django REST Framework
- MySQL database configuration
- Swagger/OpenAPI documentation at `/swagger/`
- CORS support for cross-origin requests
- Celery integration for asynchronous tasks
- Environment-based configuration using django-environ

## Setup Instructions

### Prerequisites

- Python 3.8+
- MySQL Server
- Redis (for Celery result backend)
- RabbitMQ (for Celery message broker)

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd alx_travel_app
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
```bash
cp .env.example .env
# Edit .env with your configuration
```

5. Configure MySQL database:
- Create a database named `alx_travel_app_db` (or your preferred name)
- Update database credentials in `.env`

6. Run migrations:
```bash
python manage.py makemigrations
python manage.py migrate
```

7. Create a superuser:
```bash
python manage.py createsuperuser
```

8. Run the development server:
```bash
python manage.py runserver
```

## API Documentation

Once the server is running, access the API documentation at:
- Swagger UI: http://localhost:8000/swagger/
- ReDoc: http://localhost:8000/redoc/

## Project Structure

```
alx_travel_app/
├── alx_travel_app/        # Project configuration
│   ├── settings.py        # Django settings
│   ├── urls.py           # URL routing
│   └── wsgi.py           # WSGI configuration
├── listings/             # Main app
│   ├── models.py         # Database models
│   ├── views.py          # API views
│   ├── serializers.py    # DRF serializers
│   └── urls.py           # App URL routing
├── manage.py             # Django management script
├── requirements.txt      # Python dependencies
└── .env.example         # Environment variables template
```

## Environment Variables

See `.env.example` for all required environment variables.

## License

This project is part of the ALX Software Engineering program.
