# Little Lemon Web Application

This project is the final capstone for the **Meta Back-End Developer Certificate**. It consists of building a Django-based backend for a restaurant web application, enabling reservation management, menu handling, and API-based access.

## 📌 Project Overview

The Little Lemon Web Application provides:

- A Django-based backend server
- RESTful APIs using Django REST Framework (DRF)
- Admin panel for managing reservations and menu items
- Token-based authentication for API endpoints
- Unit tests for core functionalities

## 🧰 Tech Stack

- Python 3
- Django
- Django REST Framework
- SQLite (default development database)
- Git & GitHub

## 📁 Project Structure

<pre>
<code>
Little-Lemon-Web-Application/
├── LittleLemon/               # Django project settings and URL config
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
├── restaurant/                # Django app with core business logic
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── serializers.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
│
├── db.sqlite3                 # SQLite database
├── manage.py                  # Django management script
└── README.md                  # Project documentation
</code>
</pre>


## ⚙️ Setup Instructions

1. **Clone the repository**

```bash
git clone https://github.com/lfvelascot/Little-Lemon-Web-Application.git
cd Little-Lemon-Web-Application
```

2.	Create and activate a virtual environment

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3.	Install dependencies

```bash
pip install -r requirements.txt
```

4.	Apply database migrations

```bash
python manage.py migrate
```

5.	Create superuser (optional for admin access)

```bash
python manage.py createsuperuser
```

6.	Run the development server

```bash
python manage.py runserver
```

7.	Access the app
	•	Admin panel: http://127.0.0.1:8000/admin
	•	API endpoints: http://127.0.0.1:8000/ (based on URL configuration)

🔐 Authentication

This project uses Token Authentication (via DRF). To enable it, include the following in your URLs and settings:
	•	Obtain token:

    POST /api-token-auth/

•	Use token in headers:

Authorization: Token your_token_here


🧪 Running Tests

To run unit tests:

```bash
python manage.py test
```

🛣️ API Endpoints (Examples)•	GET /menu/ – List menu items
	•	POST /menu/ – Add a new item
	•	GET /bookings/ – View reservations
	•	POST /bookings/ – Create a reservation

Note: Actual endpoints depend on the URL configuration and DRF view setup.

📝 License

This repository was created as part of the Meta Back-End Developer Capstone and is intended for educational purposes.

⸻

Developed with ❤️ by Felipe Velasco
