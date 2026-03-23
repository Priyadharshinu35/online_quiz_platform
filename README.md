# Online Quiz Platform using Django

## Project Overview
The Online Quiz Platform is a web-based application developed using Django and MySQL. It allows users to register, log in, attend quizzes, view their scores, check leaderboard rankings, and track quiz attempt history.

The system is designed to provide a simple and interactive quiz experience with category-wise quizzes, automatic score calculation, result analysis, and user performance tracking.

---

## Features

- User registration and login
- Quiz listing with search and category filter
- Quiz detail page with quiz information
- One-time quiz attempt restriction per user
- Automatic score and percentage calculation
- Quiz result and answer review
- User quiz history
- Leaderboard with quiz-based filtering
- Admin panel for managing quiz content through Django Admin
- Responsive and styled user interface

---

## Technologies Used

### Backend
- Python
- Django

### Frontend
- HTML
- CSS
- JavaScript

### Database
- MySQL

---

## Project Structure

```text
QUIZ_PLATFORM_PROJECT/
│
├── quiz_platform/
│   │
│   ├── dashboard/
│   │   ├── migrations/
│   │   ├── templates/
│   │   │   └── dashboard/
│   │   │       └── home.html
│   │   ├── admin.py
│   │   ├── apps.py
│   │   ├── models.py
│   │   ├── tests.py
│   │   ├── urls.py
│   │   └── views.py
│   │
│   ├── leaderboard/
│   │   ├── migrations/
│   │   ├── templates/
│   │   │   └── leaderboard/
│   │   │       └── leaderboard.html
│   │   ├── admin.py
│   │   ├── apps.py
│   │   ├── models.py
│   │   ├── tests.py
│   │   ├── urls.py
│   │   └── views.py
│   │
│   ├── quiz_app/
│   │   ├── migrations/
│   │   ├── templates/
│   │   │   └── quiz_app/
│   │   │       ├── quiz_list.html
│   │   │       ├── quiz_detail.html
│   │   │       ├── start_quiz.html
│   │   │       └── result.html
│   │   ├── admin.py
│   │   ├── apps.py
│   │   ├── models.py
│   │   ├── tests.py
│   │   ├── urls.py
│   │   └── views.py
│   │
│   ├── users/
│   │   ├── migrations/
│   │   ├── templates/
│   │   │   └── users/
│   │   │       ├── login.html
│   │   │       ├── register.html
│   │   │       ├── history.html
│   │   │       ├── profile.html
│   │   │       └── admin_panel.html
│   │   ├── admin.py
│   │   ├── apps.py
│   │   ├── forms.py
│   │   ├── models.py
│   │   ├── tests.py
│   │   ├── urls.py
│   │   └── views.py
│   │
│   ├── quiz_platform/
│   │   ├── __init__.py
│   │   ├── asgi.py
│   │   ├── settings.py
│   │   ├── urls.py
│   │   └── wsgi.py
│   │
│   ├── static/
│   │   ├── css/
│   │   │   └── styles.css
│   │   ├── images/
│   │   └── js/
│   │       └── timer.js
│   │
│   ├── templates/
│   │   └── base.html
│   │
│   └── manage.py
│
└── README.md


Installation Requirements

Make sure the following are installed on your system:

Python 3.x
Django 6.x
MySQL Server
MySQL Workbench
pip
Python Package Requirements

Create a file named requirements.txt and add the following:

Django==6.0.3
mysqlclient

If mysqlclient does not install properly on your system, you can use:

Django==6.0.3
PyMySQL
How to Install Requirements

Open terminal inside the project folder and run:

pip install -r requirements.txt

If you are using PyMySQL instead of mysqlclient, install with:

pip install Django==6.0.3 PyMySQL
Database Configuration

Update the MySQL settings in:

quiz_platform/quiz_platform/settings.py

Example configuration:

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'quiz_platform_db',
        'USER': 'root',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}

Make sure the database quiz_platform_db is already created in MySQL.

How to Create Database

Open MySQL Workbench and run:

CREATE DATABASE quiz_platform_db;
How to Run the Project
1. Open terminal inside project folder

Go to the folder where manage.py is present.

cd quiz_platform
2. Create virtual environment
python -m venv venv
3. Activate virtual environment
For Windows
venv\Scripts\activate
For Mac/Linux
source venv/bin/activate
4. Install dependencies
pip install -r requirements.txt
5. Apply migrations
python manage.py makemigrations
python manage.py migrate
6. Create superuser
python manage.py createsuperuser
7. Run the server
python manage.py runserver
8. Open in browser
http://127.0.0.1:8000/
How to Add Quiz Data

There are two ways to add quiz data:

Method 1: Using Django Admin

Login to Django admin panel:

http://127.0.0.1:8000/admin/

Add data in this order:

Category
Quiz
Question
Option
Method 2: Using SQL File

If you already have a prepared SQL file with categories, quizzes, questions, and options, import it into MySQL Workbench.

After importing, the data will automatically be shown on the website.

Main URLs
Home: /
Login: /users/login/
Register: /users/register/
Logout: /users/logout/
Quiz List: /quiz/
Leaderboard: /leaderboard/
User History: /users/history/
User Profile: /users/profile/
Admin Panel: /users/admin-panel/
Django Admin: /admin/
