# Personal Contacts Manager App

## Overview
This app allows users to manage their contacts (add, update, delete, and search). Built using Flask and SQLite, it demonstrates basic CRUD (Create, Read, Update, Delete) operations. 

## Technologies Used
- **Flask**: Web framework for building the application.
- **SQLite**: Lightweight database for storing contacts.
- **SQLAlchemy**: ORM (Object-Relational Mapping) library for database management.
- **HTML/CSS**: For front-end templates and styling.

## Features
- **Add Contact**: Enter a new contact with name, phone, and email.
- **Update Contact**: Modify existing contact information.
- **Delete Contact**: Remove unwanted contacts.
- **Search Contacts**: Search contacts by name, phone, or email.

## Setup Instructions

1. Clone the repository:
    ```bash
    git clone Repository_URL
    cd Repo name
    ```

2. Set up a virtual environment:
    ```bash
    python -m venv venv
    source venv/bin/activate   # (or venv\Scripts\activate on Windows)
    ```

3. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Initialize the database:
    ```bash
    python
    >>> from app import db
    >>> db.create_all()
    >>> exit()
    ```

5. Run the application:
    ```bash
    python app.py
    ```

6. Open your browser and visit `http://127.0.0.1:5000` to use the app.[link is obtained after running step 5]

## How the App Works
1. **Home Page**: Displays a list of all contacts.
    - You can **add a new contact** using the "Add New Contact" button.
    - Contacts can be **deleted** using the "Delete" link next to each contact.
    - Contacts can be **updated** using the "Edit" link next to each contact.
    - The search bar allows you to **search** by name, phone, or email.

2. **Adding/Updating Contacts**: 
    - When adding or updating a contact, enter the name, phone, and email. Click the submit button to save changes to the database.
    
3. **Error Handling**: 
    - A 404 error page is shown if a user attempts to access a page that does not exist.

## Files in the Project

### 1. `app.py`
This is the main application file where the Flask app is defined. It contains:
- **Routes**:
  - `/` - Home page showing all contacts.
  - `/add_contact` - Form to add a new contact.
  - `/delete_contact/<id>` - Deletes a contact based on its ID.
  - `/search_contacts` - Allows users to search contacts by name, phone, or email.
  - `/update_contact/<id>` - Updates contact info.
  - `@app.errorhandler(404)` - Handles 404 errors.
  
- **Database**:
  - The `Contact` model defines the structure of a contact in the database.

### 2. `requirements.txt`
This file lists all the necessary Python libraries needed to run the application. When you run `pip install -r requirements.txt`, it installs:
- **Flask**
- **SQLAlchemy**
  
### 3. `templates/`
- **`index.html`**: Displays the home page with a list of all contacts and allows users to search, update, or delete contacts.
- **`add_contact.html`**: Contains the form to add a new contact.
- **`update_contact.html`**: Contains the form to update an existing contact.
- **`error.html`**: Displays the custom 404 error page.

### 4. `static/styles.css`
The main CSS file that styles the HTML templates (contact list, forms, etc.).




---------------
My Terminal
- PS D:\Classes\OOSE\Contacts Management> git clone https://github.com/jhu-oose-f24/homework-1-Sana-Shaik-12.git
Cloning into 'homework-1-Sana-Shaik-12'...

remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (3/3), done.
- PS D:\Classes\OOSE\Contacts Management> python -m venv venv

Error: [Errno 13] Permission denied: 'D:\\Classes\\OOSE\\Contacts Management\\venv\\Scripts\\python.exe'
- PS D:\Classes\OOSE\Contacts Management> venv\Scripts\activate

(venv) PS D:\Classes\OOSE\Contacts Management> pip install -r requirements.txt

Requirement already satisfied: Flask==2.1.2 in d:\classes\oose\contacts management\venv\lib\site-packages (from -r requirements.txt (line 1)) (2.1.2)
Requirement already satisfied: Werkzeug==2.0.3 in d:\classes\oose\contacts management\venv\lib\site-packages (from -r requirements.txt (line 2)) (2.0.3)
Requirement already satisfied: Flask-SQLAlchemy==2.5.1 in d:\classes\oose\contacts management\venv\lib\site-packages (from -r requirements.txt (line 3)) (2.5.1)
Requirement already satisfied: SQLAlchemy==1.4.49 in d:\classes\oose\contacts management\venv\lib\site-packages (from -r requirements.txt (line 4)) (1.4.49)
Requirement already satisfied: Jinja2>=3.0 in d:\classes\oose\contacts management\venv\lib\site-packages (from Flask==2.1.2->-r requirements.txt (line 1)) (3.1.4)
Requirement already satisfied: itsdangerous>=2.0 in d:\classes\oose\contacts management\venv\lib\site-packages (from Flask==2.1.2->-r requirements.txt (line 1)) (2.2.0)
Requirement already satisfied: click>=8.0 in d:\classes\oose\contacts management\venv\lib\site-packages (from Flask==2.1.2->-r requirements.txt (line 1)) (8.1.7)
Requirement already satisfied: greenlet!=0.4.17 in d:\classes\oose\contacts management\venv\lib\site-packages (from SQLAlchemy==1.4.49->-r requirements.txt (line 4)) (3.1.0)
Requirement already satisfied: colorama in d:\classes\oose\contacts management\venv\lib\site-packages (from click>=8.0->Flask==2.1.2->-r requirements.txt (line 1)) (0.4.6)
Requirement already satisfied: MarkupSafe>=2.0 in d:\classes\oose\contacts management\venv\lib\site-packages (from Jinja2>=3.0->Flask==2.1.2->-r requirements.txt (line 1)) (2.1.5)
- (venv) PS D:\Classes\OOSE\Contacts Management> python

Python 3.12.5 (tags/v3.12.5:ff3bc82, Aug  6 2024, 20:45:27) [MSC v.1940 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
- >>> from app import db

D:\Classes\OOSE\Contacts Management\venv\Lib\site-packages\flask_sqlalchemy\__init__.py:872: FSADeprecationWarning: SQLALCHEMY_TRACK_MODIFICATIONS adds significant overhead and will be disabled by default in the future.  Set it to True or False to suppress this warning.
  warnings.warn(FSADeprecationWarning(
- >>> db.create_all()
- >>> exit()
- (venv) PS D:\Classes\OOSE\Contacts Management> python app.py

D:\Classes\OOSE\Contacts Management\venv\Lib\site-packages\flask_sqlalchemy\__init__.py:872: FSADeprecationWarning: SQLALCHEMY_TRACK_MODIFICATIONS adds significant overhead and will be disabled by default in the future.  Set it to True or False to suppress this warning.
  warnings.warn(FSADeprecationWarning(
  Serving Flask app 'app' (lazy loading)
  Environment: production
   WARNING: This is a development server. Do not use it in a production deployment.
   Use a production WSGI server instead.
  Debug mode: on
  Restarting with stat
D:\Classes\OOSE\Contacts Management\venv\Lib\site-packages\flask_sqlalchemy\__init__.py:872: FSADeprecationWarning: SQLALCHEMY_TRACK_MODIFICATIONS adds significant overhead and will be disabled by default in the future.  Set it to True or False to suppress this warning.
  warnings.warn(FSADeprecationWarning(
  Debugger is active!
  Debugger PIN: 958-650-593
  Running on **http://127.0.0.1:5000/** (Press CTRL+C to quit)
127.0.0.1 - - [16/Sep/2024 18:50:29] "GET / HTTP/1.1" 200 -
127.0.0.1 - - [16/Sep/2024 18:50:29] "GET /static/styles.css HTTP/1.1" 304 
