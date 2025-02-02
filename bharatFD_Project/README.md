Django FAQ Management System with Multilingual Support
This project is a Django-based FAQ management system that supports multilingual content, WYSIWYG editor integration, and efficient caching mechanisms. It includes a REST API for managing FAQs and provides language-specific translations using Google Translate API.

Features
FAQ Model: Stores FAQs with questions and answers, supporting multilingual translations.

WYSIWYG Editor: Integrated with django-ckeditor for rich text formatting.

REST API: Supports language-specific FAQ retrieval via query parameters.

Caching: Uses Redis to cache translations for improved performance.

Multilingual Support: Automates translations using Google Translate API with fallback to English.

Admin Panel: User-friendly interface for managing FAQs.

Unit Tests: Comprehensive test coverage for models and API endpoints.

PEP8 Compliance: Follows Python best practices and coding standards.

Docker Support: Includes Dockerfile and docker-compose.yml for easy deployment.

Installation
Prerequisites
Python 3.8+

Redis

Docker (optional)

Steps
Clone the repository:

git clone https://github.com/yourusername/django-faq-system.git
cd django-faq-system
Set up a virtual environment:


python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies:


pip install -r requirements.txt
Set up environment variables:
Create a .env file in the root directory and add the following:


DEBUG=True
REDIS_URL=redis://localhost:6379/1

Run migrations:
python manage.py migrate
Start the development server:


python manage.py runserver
Access the admin panel:

Create a superuser:
python manage.py createsuperuser
Visit http://localhost:8000/admin to manage FAQs.

API Usage
Fetch FAQs
Default (English):


curl http://localhost:8000/api/faqs/
Hindi:


curl http://localhost:8000/api/faqs/?lang=hi
Bengali:


curl http://localhost:8000/api/faqs/?lang=bn
Caching
The system uses Redis to cache translations. To clear the cache:

python manage.py clear_cache
Docker Deployment
Build and run the Docker container:


docker-compose up --build
Access the application:

Visit http://localhost:8000 in your browser.

Testing
Run unit tests using pytest:

# BharathFd-project
