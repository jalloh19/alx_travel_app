# ALX Travel App

Backend scaffolding for the ALX Travel application built with Django and Django REST Framework.

## Getting Started

1. Create and activate a virtual environment.
2. Install requirements: `pip install -r requirements.txt`.
3. Copy `.env.example` to `.env` and update the database and broker credentials.
4. Run migrations: `python manage.py migrate`.
5. Start the server: `python manage.py runserver`.

Swagger documentation is available at `/swagger/` once the development server is running. Celery is configured to use RabbitMQ by default; update the `CELERY_BROKER_URL` if you prefer a different broker.
