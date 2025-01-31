# Product Management API (Django)

This is the backend of the Product Management Application built using Django and Django Rest Framework.


## Prerequisites

- Python 3.x installed
- pip (Python package manager)
- Virtual environment (optional but recommended)


## Installation & Setup

1. **Clone the repository**  
   git clone <repository-url>
   cd backend

2. **Create a virtual environment (optional but recommended)**
    python -m venv venv
    source venv/bin/activate  # On Windows use: venv\Scripts\activate

3. **Install dependencies**
    pip install -r requirements.txt

4. **Apply migrations**
    python manage.py makemigrations
    python manage.py migrate

5. **Run the development server**
    python manage.py runserver
    The API will be available at http://127.0.0.1:8000/api/products/.


## API Endpoints
Method	    Endpoint                Description
GET         /api/products/	        Fetch all products
POST        /api/products/	        Add a new product
PUT         /api/products/<id>/	    Update an existing product
DELETE	    /api/products/<id>/	    Delete a product


## CORS Configuration
    If the frontend throws a CORS error, ensure that Django CORS headers are installed and configured in settings.py:

1. Install django-cors-headers if not already installed:
    pip install django-cors-headers

2. Add it to INSTALLED_APPS in settings.py:
    INSTALLED_APPS = [
        ...
        'corsheaders',
    ]

3. Add middleware:
    MIDDLEWARE = [
        ...
        'corsheaders.middleware.CorsMiddleware',
    ]

4. Allow frontend access (modify if necessary):
    CORS_ALLOWED_ORIGINS = [
        "http://localhost:3000",
    ]