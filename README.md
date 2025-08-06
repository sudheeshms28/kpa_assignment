# KPA Assignment API

This is a Django REST API built for the KPA Assignment.  
It allows users to:

- Add new student data
- Add new user data

---

##   Tech Stack

- Python 3
- Django 4+
- Django REST Framework
- PostgreSQL

---

##   Project Setup

### 1. Clone the Repository

```bash
git clone https://github.com/sudheeshms28/kpa_assignment.git
cd kpa_assignment
```

### 2. Create Virtual Environment & Install Dependencies

```bash
 # On Windows
python -m venv env
env\Scripts\activate         
pip install -r requirements.txt
```

> If `requirements.txt` is missing, manually install:
```bash
pip install django djangorestframework psycopg2-binary
```

---

##   Database Setup

Make sure PostgreSQL is installed on your system and a database is created.

Example `settings.py` configuration:
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'your_db_name',
        'USER': 'your_db_user',
        'PASSWORD': 'your_db_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

---

##   Run Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

---

##   Start the Server

```bash
python manage.py runserver
```

Server will run at:  
`http://localhost:8000/`

---

##   API Endpoints

###   Add Student

- **URL:** `http://localhost:8000/add-student/`  
- **Method:** `POST`  
- **Headers:**  
  `Content-Type: application/json`

**Request Body:**
```json
{
  "name": "Anoop",
  "email": "anoop@example.com",
  "phone": "9876543210",
  "course": "Maths"
}
```

**Response:**
```json
{
  "message": "Student added successfully",
  "student": {
    "id": 1,
    "name": "Anoop",
    "email": "anoop@example.com",
    "phone": "9876543210",
    "course": "Maths"
  }
}
```

---

###   Add User

- **URL:** `http://localhost:8000/add-user/`  
- **Method:** `POST`  
- **Headers:**  
  `Content-Type: application/json`

**Request Body:**
```json
{
  "username": "Rajesh",
  "email": "rajesh1@gmail.com",
  "password": "000999"
}
```

**Response:**
```json
{
  "message": "User created successfully",
  "username": "Rajesh",
  "email": "rajesh1@gmail.com"
}
```

---

##  Author

 **Sudheesh**  
Email: [sudheesh090807@gmail.com](mailto : sudheesh090807@gmail.com)

---

##  Notes

- Make sure PostgreSQL server is running before starting the Django server.
- All API testing can be done using [Thunder Client](https://www.thunderclient.com/) or Postman.


##  About Me

I am a self-motivated fresher who recently completed a course in Python and Django development.  
This project was developed as part of an assignment to practice building real-world REST APIs using Django and PostgreSQL.

Throughout the development process, I referred to official documentation and online resources to understand best practices and implement them effectively.

This project helped me gain hands-on experience with Django REST Framework, and I am continuously learning and improving my skills in backend development.


---