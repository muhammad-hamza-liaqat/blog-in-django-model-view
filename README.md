# Blog Application

A simple Django-based blog application to create, read, update, and delete blog posts.

## Features

- Create, update, and delete blog posts.
- View a list of all blog posts with metadata (creation and update timestamps).
- User-friendly design with confirmation prompts for destructive actions.

---

## Installation and Setup

### Prerequisites

- Python 3.8+ installed
- pip (Python package manager)
- Virtual environment tool (`venv` or similar)
- PostgreSQL (optional for production)

---

### 1. Clone the Repository

```bash
git clone https://github.com/muhammad-hamza-liaqat/blog-in-django-model-view
cd blog-app
```

---

### 2. Create and Activate a Virtual Environment

```bash
python -m venv venv
# Activate the virtual environment:
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Setup the Database

#### Using SQLite (default):

No additional configuration is required. The app uses SQLite by default.

#### Using PostgreSQL (optional):

1. Install PostgreSQL and create a database.
2. Update the `DATABASES` configuration in `settings.py`:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'your_database_name',
        'USER': 'your_database_user',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

---

### 5. Run Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

---

### 6. Create a Superuser

```bash
python manage.py createsuperuser
```

Follow the prompts to set up a username, email, and password.

---

### 7. Run the Development Server

```bash
python manage.py runserver
```

Visit `http://127.0.0.1:8000/` in your web browser to access the application.

---

## Additional Notes

### Static Files

Collect static files (for production environments):

```bash
python manage.py collectstatic
```

### Environment Variables

Create a `.env` file in the project root to manage sensitive settings like `SECRET_KEY`, `DEBUG`, and `DATABASE_URL`. Example:

```
SECRET_KEY=your-secret-key
DEBUG=True
```

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.
