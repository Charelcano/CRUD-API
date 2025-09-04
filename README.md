# CRUD API Project  

## Project Overview  
This project is a simple **CRUD (Create, Read, Update, Delete) API** built with **Node.js, Express, and MySQL**.  
It manages two entities: **Students** and **Courses**.  
The project demonstrates RESTful API design, modular controllers, and route handling.  

---

## Setup Steps  

git clone https://github.com/Charelcano/CRUD-API.git
cd CRUD-API

2. Install dependencies
npm install

3. Setup environment variables

Create a `.env` file in the project root with your database connection:

```env
DB_HOST=localhost
DB_USER=root
DB_PASS=
DB_NAME=lab_crud
PORT=3000



(You can also check .env.example for placeholder values.)

4. Setup the database

In MySQL, create the database and table:

```sql
CREATE DATABASE lab_crud;

USE lab_crud;

CREATE TABLE IF NOT EXISTS students (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  email VARCHAR(100) NOT NULL UNIQUE,
  course VARCHAR(50),
  year_level INT
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;


-- How to Run

Start the server in development mode:

npm run dev


Or in production mode:

npm start


By default, the server runs at:

http://localhost:3000

-- API Endpoints

Base URL: /api

Students
Method	Endpoint	Description
GET	/students	Get all students
GET	/students/:id	Get student by ID
POST	/students	Create new student
PUT	/students/:id	Update existing student
DELETE	/students/:id	Delete student by ID
Health Check
Method	Endpoint	Description
GET	/health	Check API + DB status
