# 🔐 Flask User Authentication with Admin Panel This is a Flask-based web application that provides user **registration**, **login**, **logout**, and an **admin dashboard** using **Flask-Admin**. It uses **MySQL** for database storage and **Flask-Login** for session handling. --- ## 🧰 Tech Stack - **Flask** – Micro web framework - **Flask-WTF** – Form handling and CSRF protection - **Flask-Login** – User session management - **Flask-Admin** – Admin dashboard - **SQLAlchemy** – ORM for database interaction - **MySQL** – Relational database --- ## 📂 Folder Structure Rover-DIP3/ ├── apps/ │ ├── authentication/ │ ├── dashboard/ │ ├── home/ │ ├── reports/ │ ├── static/ │ ├── suppression/ │ ├── templates/ │ ├── templatetags/ │ └── transform/ ├── core/ ├── media/ ├── staticfiles/ ├── venv/ ├── manage.py ├── requirements.txt ├── .gitignore └── README.md yaml Copy Edit --- ## ⚙️ Setup Instructions ### ✅ 1. Clone the repository ```bash git clone https://github.com/hiteshbhamre07/DIP_3.git cd DIP_3 🐍 2. Create and activate virtual environment bash Copy Edit python "-m" venv venv venv\Scripts\activate # On Windows 📦 3. Install dependencies bash Copy Edit pip install "-r" requirements.txt 🔧 4. Configure database Make sure MySQL is installed and running. Create a database named flaskapp_db. Update your database URI in the main Flask script: python Copy Edit app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql://root:root@localhost/flaskapp_db' Then initialize the database: bash Copy Edit python >>> from your_script_name import db >>> db.create_all() >>> exit() Replace your_script_name with the name of your Python file (e.g. app.py). 🚀 Running the Application bash Copy Edit python your_script_name.py Visit the app in your browser at: cpp Copy Edit http://127.0.0.1:5000/ 👤 User Functionality ✅ User Registration ✅ Login and Logout ✅ Session handling with Flask-Login ✅ Password encryption using generate_password_hash ✅ CSRF protection with Flask-WTF 🛠 Admin Panel Built using Flask-Admin Access via: /admin/login Protected by login credentials Full CRUD access to user data (except password) 🔐 Default Admin Credentials (for testing) ⚠️ Replace these in production with secure admin credentials! makefile Copy Edit Email: admin@example.com Password: admin123 Update logic in /admin/login route to validate real admin users. ✅ Features Overview Modular and Clean Flask Structure Secure Form Handling ORM-powered MySQL Interaction Simple Bootstrap-based UI Admin CRUD Access to User Table
Flask user authentication and admin panel: key features and setup
This project outlines a Flask-based web application providing user authentication (registration, login, logout) and an admin dashboard using Flask-Admin. It relies on MySQL for database storage and Flask-Login for user session management. 
Key features
User Registration: Allows new users to create accounts within the application.
Login and Logout: Enables users to securely log in and out of the application, managing their sessions with Flask-Login.
Secure Session Handling: Uses Flask-Login to manage user sessions, ensuring secure and persistent logins.
Password Encryption: Employs password hashing, specifically with generate_password_hash (often backed by a library like Werkzeug or Bcrypt) to store user passwords securely. Storing passwords in plaintext is a security risk.
CSRF Protection: Implements Cross-Site Request Forgery (CSRF) protection using Flask-WTF to secure forms and prevent malicious attacks.
Admin Dashboard: Provides an administrative interface built with Flask-Admin, accessible via /admin/login.
Admin Panel Security: The admin panel is secured with login credentials, ensuring only authorized administrators can access it.
CRUD for User Data: The admin panel allows full Create, Read, Update, and Delete (CRUD) operations on user data, with the exception of passwords, which are securely stored and shouldn't be directly editable in plain text.
Modular Flask Structure: Follows a structured approach, potentially using Flask Blueprints and the Application Factory pattern for better code organization and scalability.
MySQL Database: Utilizes MySQL as the relational database for storing application data, including user information.
ORM Interaction (SQLAlchemy): Uses SQLAlchemy, an Object Relational Mapper (ORM), simplifying database interactions and allowing developers to work with Python objects instead of raw SQL queries.
Simple UI: Features a basic user interface, possibly built with a framework like Bootstrap. 
Setup instructions
Clone the Repository:
bash
git clone https://github.com/hiteshbhamre07/DIP_3.git
cd DIP_3
```
Use code with caution.

Create and Activate Virtual Environment:
bash
python -m venv venv
venv\Scripts\activate # On Windows
```
Use code with caution.

Install Dependencies:
bash
pip install -r requirements.txt
```
Use code with caution.

Configure Database:
Ensure MySQL is installed and running.
Create a database named flaskapp_db.
Update your database URI in the main Flask script (e.g., app.py):
python
app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql://root:root@localhost/flaskapp_db' 
```
Use code with caution.

Initialize the database (replace your_script_name with the actual filename):
bash
python
>>> from your_script_name import db
>>> db.create_all()
>>> exit()
```
Use code with caution.

Running the Application:
bash
python your_script_name.py
```
*   Visit the app in your browser at `http://127.0.0.1:5000/`.
*   Access the admin panel at `/admin/login`.

Use code with caution.

 
Admin credentials (for testing)
Email: admin@example.com
Password: admin123
