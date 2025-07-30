# 🔐 Flask User Authentication with Admin Panel

This is a Flask-based web application that provides user **registration**, **login**, **logout**, and an **admin dashboard** using **Flask-Admin**. It uses **MySQL** for database storage and **Flask-Login** for session handling.

---

## 🧰 Tech Stack

- **Flask** – Micro web framework  
- **Flask-WTF** – Form handling and CSRF protection  
- **Flask-Login** – User session management  
- **Flask-Admin** – Admin dashboard  
- **SQLAlchemy** – ORM for database interaction  
- **MySQL** – Relational database  

---

**## 📂 Folder Structure                                         =

Rover-DIP3/                                --Main Project  Directory
├── apps/                                  --app folder  
│ ├── authentication/
│ ├── dashboard/
│ ├── home/
│ ├── reports/
│ ├── static/
│ ├── suppression/
│ ├── templates/
│ ├── templatetags/
│ └── transform/
├── core/                                   ---main Project 
├── media/
├── staticfiles/
├── venv/
├── manage.py
├── requirements.txt
├── .gitignore  
└── README.md                                               =

## ⚙️ Setup Instructions

### ✅ 1. Clone the repository

```bash
git clone https://github.com/hiteshbhamre07/DIP_3.git
cd DIP_3

**🐍 2. Create and activate virtual environment**
python -m venv venv
venv\Scripts\activate  # On Windows

**📦 3. Install dependencies**
pip install -r requirements.txt

**🔧 4. Configure database**
Make sure MySQL is installed and running. Create a database named flaskapp_db.

Update your database URI in the main Flask script:
app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql://root:root@localhost/flaskapp_db'
Then initialize the database:

python
>>> from your_script_name import db
>>> db.create_all()
>>> exit()
Replace your_script_name with the name of your Python file (e.g. app.py).

🚀 Running the Application
python your_script_name.py

Visit the app in your browser at:
http://127.0.0.1:5000/


**👤 User Functionality**
✅ User Registration

✅ Login and Logout

✅ Session handling with Flask-Login

✅ Password encryption using generate_password_hash

✅ CSRF protection with Flask-WTF


🛠 Admin Panel
Built using Flask-Admin

Access via: /admin/login

Protected by login credentials

Full CRUD access to user data (except password)

🔐 Default Admin Credentials (for testing)
⚠️ Replace these in production with secure admin credentials!

makefile
Email: admin@example.com  
Password: admin123
Update logic in /admin/login route to validate real admin users.

✅ Features Overview
Modular and Clean Flask Structure

Secure Form Handling

ORM-powered MySQL Interaction

Simple Bootstrap-based UI

Admin CRUD Access to User Table
