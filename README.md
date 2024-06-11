ToDo List App
This is a simple ToDo List application built with Node.js, Express, EJS, and PostgreSQL. It allows users to add, edit, and delete items from their to-do list.

Features
Add new items to the to-do list
Edit existing items
Delete items from the list
Dynamic user interface
Technologies Used
Node.js
Express
EJS (Embedded JavaScript templating)
PostgreSQL
HTML/CSS
Prerequisites
Before running this project, ensure you have the following installed:

Node.js
PostgreSQL
Getting Started
Clone the repository:

bash
Copy code
git clone https://github.com/thesauravsingh/todolist-app.git
cd todolist-app
Install dependencies:

bash
Copy code
npm install
Set up the PostgreSQL database:

Start your PostgreSQL server.
Create a new database:
sql
Copy code
CREATE DATABASE todolist;
Create a table for storing the to-do items:
sql
Copy code
CREATE TABLE items (
  id SERIAL PRIMARY KEY,
  title VARCHAR(255) NOT NULL
);
Configure the database connection:

Update the database connection details in the index.js file:

javascript
Copy code
const db = new pg.Client({
  user: "postgres",
  host: "localhost",
  database: "todolist",
  password: "your-password",
  port: 5432,
});
db.connect();
Run the application:

bash
Copy code
npm start
Access the application:

Open your browser and navigate to http://localhost:3000.

Project Structure
css
Copy code
.
├── public
│   └── assets
│       └── icons
│           ├── check-solid.svg
│           └── pencil-solid.svg
├── views
│   ├── partials
│   │   ├── header.ejs
│   │   └── footer.ejs
│   └── index.ejs
├── node_modules
├── index.js
├── package.json
└── README.md
Code Overview
index.js
This is the main file that sets up the Express server, connects to the PostgreSQL database, and defines the routes for the application.

views/index.ejs
This is the main view file that renders the to-do list. It uses EJS templating to dynamically display the list items and forms for adding, editing, and deleting items.

views/partials/header.ejs and views/partials/footer.ejs
These files contain the header and footer sections of the HTML template, included in index.ejs.

public/assets/icons
This directory contains the icon images used in the application.

Routes
GET / - Retrieves and displays the list of to-do items.
POST /add - Adds a new item to the list.
POST /edit - Updates an existing item's title.
POST /delete - Deletes an item from the list.
License
This project is licensed under the MIT License. See the LICENSE file for details.

Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

Acknowledgments
This project is based on a Udemy Web Development course.
