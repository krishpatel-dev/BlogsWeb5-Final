# 🐍 Flask Blog with User Authentication - Day 69

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/downloads/)
[![Flask](https://img.shields.io/badge/flask-2.3.2-000000.svg?logo=flask)](https://flask.palletsprojects.com/)
[![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-2.0.25-333333.svg?logo=sqlalchemy)](https://www.sqlalchemy.org/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/krishpatel-dev/BlogsWeb5-Final.git/graphs/commit-activity)

A feature-rich blog application built with Flask, featuring user authentication, blog post management, and comment system.

## 📋 Table of Contents
- [Features](#-features)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Environment Setup](#environment-setup)
  - [Running the Application](#running-the-application)
- [Project Structure](#-project-structure)
- [Technologies Used](#-technologies-used)
- [API Endpoints](#-api-endpoints)
- [Contributing](#-contributing)

## ✨ Features

- **User Authentication**
  - User registration and login/logout
  - Secure password hashing
  - Protected routes for authenticated users
  - Admin-only access for post management

- **Blog Functionality**
  - Create, Read, Update, and Delete blog posts (Admin only)
  - View all posts on the home page
  - Individual post pages with unique URLs
  - Rich text editing with CKEditor
  - Responsive design with Bootstrap 5

- **Comments System**
  - Authenticated users can post comments
  - Gravatar integration for user avatars
  - Real-time comment display

## 🛠 Getting Started

### Prerequisites
- Python 3.8 or higher
- pip (Python package installer)

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
   cd Day-69
   ```

2. **Set up a virtual environment (recommended)**
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

### Environment Setup

1. Create a [.env](cci:7://file:///e:/Complete%20Python%20Course/Day%2069/.env:0:0-0:0) file in the project root
2. Generate a secret key using the provided [secretKeyGenerater.py](cci:7://file:///e:/Complete%20Python%20Course/Day%2069/secretKeyGenerater.py:0:0-0:0)
3. Add the following to your [.env](cci:7://file:///e:/Complete%20Python%20Course/Day%2069/.env:0:0-0:0) file:
   ```
   SECRET_KEY=your_generated_secret_key
   ```

### Running the Application

1. **Initialize the database**
   ```bash
   python
   >>> from main import app, db
   >>> with app.app_context():
   ...     db.create_all()
   ```

2. **Start the development server**
   ```bash
   python main.py
   ```

3. **Open your browser and visit**
   ```
   http://127.0.0.1:5001
   ```

## 📁 Project Structure

```
Day-69/
├── instance/              # Database instance
├── static/               # Static files (CSS, JS, images)
├── templates/            # HTML templates
│   ├── about.html
│   ├── contact.html
│   ├── header.html
│   ├── footer.html
│   ├── index.html
│   ├── login.html
│   ├── make-post.html
│   ├── post.html
│   └── register.html
├── .env                 # Environment variables
├── .gitignore
├── forms.py             # WTForms definitions
├── main.py              # Main application file
├── requirements.txt     # Project dependencies
└── secretKeyGenerater.py # Utility for generating secret keys
```

## 🔧 Technologies Used

- **Backend**
  - Flask 2.3.2
  - SQLAlchemy 2.0.25
  - Flask-Login 0.6.3
  - Flask-WTF 1.2.1
  - Flask-CKEditor 0.4.6
  - Flask-Gravatar 0.5.0

- **Frontend**
  - Bootstrap 5
  - CKEditor 4
  - Gravatar for user avatars
  - HTML5 & CSS3

## 🌐 API Endpoints

| Method | Endpoint            | Description                          | Auth Required |
|--------|---------------------|--------------------------------------|---------------|
| GET    | /                   | Home page with all posts             | No            |
| GET    | /post/<post_id>     | View a specific post with comments   | No            |
| GET    | /register           | User registration form               | No            |
| POST   | /register           | Create new user account              | No            |
| GET    | /login              | User login form                      | No            |
| POST   | /login              | Authenticate user                    | No            |
| GET    | /logout             | Logout current user                  | Yes           |
| GET    | /new-post           | Form to create a new post            | Admin only    |
| POST   | /new-post           | Create a new post                    | Admin only    |
| GET    | /edit-post/<post_id>| Form to edit a post                  | Admin only    |
| POST   | /edit-post/<post_id>| Update a post                        | Admin only    |
| GET    | /delete/<post_id>   | Delete a post                        | Admin only    |
| POST   | /post/<post_id>     | Add a comment to a post              | Yes           |
| GET    | /about              | About page                           | No            |
| GET    | /contact            | Contact page                         | No            |

## 🤝 Contributing

Contributions are welcome! Here's how you can contribute:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

<div align="center">
  Made with ❤️ and ☕ by <b>Krish</b>
</div>