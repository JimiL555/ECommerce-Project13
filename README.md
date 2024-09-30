# My-Project-13


E-commerce Back-End

Description

The E-commerce Back-End project provides the back-end functionality for an online retail platform. This project was developed using Node.js, Express.js, and Sequelize (a promise-based ORM) to interact with a PostgreSQL database. The project includes full CRUD operations for categories, products, and tags, providing a robust back-end system for managing an e-commerce store.

This project is a challenge from the Full Stack Web Development Bootcamp and focuses on building out the back end for an e-commerce site. The front end is not provided or required for this challenge. Instead, the project focuses on API functionality for managing product data in the database.

Table of Contents

	1.	Description
	2.	Technologies Used
	3.	Installation
	4.	Usage
	5.	API Routes
	6.	Database Models
	7.	Seeding the Database
	8.	Walkthrough Video
	9.	Contributing
	10.	Questions

Technologies Used

	•	Node.js: A JavaScript runtime built on Chrome’s V8 engine that allows for server-side execution of JavaScript.
	•	Express.js: A lightweight web framework for Node.js used for handling routes, middleware, and server-side logic.
	•	Sequelize: A promise-based ORM (Object-Relational Mapping) used to map models to PostgreSQL tables, enabling CRUD operations on database entities.
	•	PostgreSQL: A powerful, open-source object-relational database used to store and manage product, category, and tag data.
	•	dotenv: Used to load environment variables from a .env file for secure storage of sensitive data such as database credentials.

Installation

Prerequisites

Make sure you have the following installed on your system:

	•	Node.js (version 12 or higher)
	•	PostgreSQL (version 13 or higher)
	•	npm (comes with Node.js)
	•	Insomnia or Postman (for API testing)

Steps:

	1.	Clone the repository:
        git clone https://github.com/JimiL555/My-Project-13.git

	2.	Navigate to the project directory:
        cd My-Project-13

	3.	Install dependencies:
        npm install

	4.	Set up environment variables:
        Create a .env file in the root of your project and add the following:
        DB_NAME='ecommerce_db'
        DB_USER='postgres'
        DB_PASSWORD='your_password'
        DB_HOST='localhost'
        DB_PORT='5432'

    5.	Create the PostgreSQL database:
	•	Open the PostgreSQL shell or a GUI tool like pgAdmin.
	•	Create the database using the following command:
        CREATE DATABASE ecommerce_db;

    6.	Run the database schema to set up the tables:
        psql -U postgres -d ecommerce_db -f db/schema.sql


Usage

	1.	Start the server:
        npm start - This will start the Express server and sync all Sequelize models with the PostgreSQL database.

	2.	Test API routes using Insomnia or Postman.
	•	Example URL for testing:
            http://localhost:3001/api/categories



For testing the API, use the GET, POST, PUT, and DELETE methods to interact with the categories, products, and tags.

API Routes

Here’s an overview of the available API routes:

Categories:

	•	GET /api/categories: Get all categories.
	•	GET /api/categories/:id: Get a single category by ID.
	•	POST /api/categories: Create a new category.
	•	PUT /api/categories/:id: Update a category by ID.
	•	DELETE /api/categories/:id: Delete a category by ID.

Products:

	•	GET /api/products: Get all products.
	•	GET /api/products/:id: Get a single product by ID.
	•	POST /api/products: Create a new product.
	•	PUT /api/products/:id: Update a product by ID.
	•	DELETE /api/products/:id: Delete a product by ID.

Tags:

	•	GET /api/tags: Get all tags.
	•	GET /api/tags/:id: Get a single tag by ID.
	•	POST /api/tags: Create a new tag.
	•	PUT /api/tags/:id: Update a tag by ID.
	•	DELETE /api/tags/:id: Delete a tag by ID.

Database Models

There are four models in this project:

	1.	Category:
	•	id: Integer, Primary Key, Auto Increment.
	•	category_name: String, Required.
	2.	Product:
	•	id: Integer, Primary Key, Auto Increment.
	•	product_name: String, Required.
	•	price: Decimal, Required.
	•	stock: Integer, Default 10.
	•	category_id: Integer, Foreign Key to Category model.
	3.	Tag:
	•	id: Integer, Primary Key, Auto Increment.
	•	tag_name: String.
	4.	ProductTag (Join Table):
	•	id: Integer, Primary Key, Auto Increment.
	•	product_id: Integer, Foreign Key to Product model.
	•	tag_id: Integer, Foreign Key to Tag model.

Model Relationships:

	•	Category has many Products.
	•	Product belongs to Category.
	•	Product belongs to many Tags (through ProductTag).
	•	Tag belongs to many Products (through ProductTag).

Seeding the Database

To seed the database with sample data for testing:

	1.	Run the following command:
        npm run seed


Walkthrough Video

A full walkthrough video demonstrating how to:

	•	Create the PostgreSQL database.
	•	Seed the database with test data.
	•	Start the server and run API requests.
	•	Test GET, POST, PUT, DELETE routes.

Link to the walkthrough video: 
        https://youtu.be/c78yDuC-JO8?si=fFS-r_FXgfiupzKi

Contributing

If you’d like to contribute to this project, feel free to fork the repository and submit a pull request. Please follow the project’s structure and include detailed commit messages.

Questions

If you have any questions, feel free to reach out to me at:
    liapis.jsl@gmail.com
    	•	GitHub: JimiL555