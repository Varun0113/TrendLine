**Django News Platform with Authentication & Feature Locking**

This project is a Django-based news web application that delivers category-wise news using the NewsAPI.
It is designed with a clear distinction between public users and authenticated users, where advanced features are intentionally locked behind login to improve user engagement and platform value.
The application focuses on clean architecture, basic security practices, and a scalable foundation for future enhancements.

Project Overview

The platform allows users to browse news content with limited access on the home page. After registering and logging in, users gain access to an expanded dashboard featuring more news categories, an AI chatbot, and curated sidebars for recent and trending news.
This approach reflects a real-world product model rather than an open-access demo application.

Key Features

Public Access (Home Page)
⦁	Limited number of news categories
⦁	AI chatbot and premium features locked
⦁	Encourages users to register or log in for full access

User Authentication
⦁	User registration and login system
⦁	Password validation rules:
	Minimum 8 characters
	Password confirmation matching
	Username cannot be part of the password
	Basic checks to prevent weak credentials
⦁	Session-based authentication using Django’s built-in system

Authenticated Dashboard
⦁	Access to 15 news categories
⦁	Fully unlocked AI chatbot
⦁	Sidebar sections:
	Recent news
	Trending news
⦁	Improved layout and richer user experience

Technology Stack
⦁	Backend: Django (Python)
⦁	Frontend: HTML, CSS, JavaScript
⦁	API Integration: NewsAPI (newsapi.org)
⦁	Database: SQLite3
⦁	Authentication: Django Auth System
⦁	Templating: Django Template Engine

Project Structure

MYPROJECT/
│
├── media/
├── static/
├── templates/
│   └── trendline/
│       ├── base.html
│       ├── home.html
│       ├── login.html
│       ├── register.html
│       └── dashboard.html
│
├── trendline/
│   ├── migrations/
│   ├── static/
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── urls.py
│   └── views.py
│
├── db.sqlite3
├── manage.py
└── README.md

Installation and Setup

1. Clone the Repository
git clone https://github.com/your-username/TrendLine.git
cd TrendLine

2. Create a Virtual Environment (Recommended)
python -m venv venv
source venv/bin/activate   # Linux / macOS
venv\Scripts\activate      # Windows

3. Install Dependencies
pip install django requests

4. Configure NewsAPI
Create an account at https://newsapi.org
Generate an API key
Add the key to your Django settings or environment variables

Example:
NEWS_API_KEY = "your_api_key_here"

5. Run Database Migrations
python manage.py migrate

6. Start the Development Server
python manage.py runserver

Access the application at:
http://127.0.0.1:8000/

Security Notes
⦁	Enforces basic password validation rules
⦁	Prevents common weak-password patterns
⦁	Uses Django’s built-in session management
⦁	Feature access is restricted for unauthenticated users

Expected Outcome
⦁	Clear separation between public and authenticated users
⦁	Improved user engagement through feature locking
⦁	Clean and maintainable Django project structure
⦁	Strong foundation for future expansion

Author
Varun Goyal
