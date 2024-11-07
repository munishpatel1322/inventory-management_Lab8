# inventory-management_Lab8

This is a Laravel-based Inventory Management System application, designed as part of a web development lab assignment. The project allows users to perform CRUD (Create, Read, Update, Delete) operations on inventory items. It is deployed locally using Podman or Docker containers and demonstrates key Laravel concepts such as MVC structure, routing, middleware, and dependency injection.

Table of Contents
Project Overview
Features
Requirements
Installation
Usage
Deployment with Podman
Contributing
License
Project Overview
This Inventory Management System provides an easy way for users to manage inventory items in a store setting. It leverages Laravel’s 11.x framework architecture, focusing on MVC principles, routing, and middleware.

Features
Add new inventory items with name, category, quantity, and price.
Update details of existing items.
Delete items from the inventory.
View a list of all items in an organized table format.
Requirements
PHP 8.0 or higher
Composer
Laravel 11.x
MySQL (or another compatible database)
Podman or Docker for containerization
Installation
Clone the Repository:

bash
Copy code
git clone https://github.com/your-username/inventory-management_Lab8.git
cd inventory-management_Lab8
Install Composer Dependencies:

bash
Copy code
composer install
Copy the .env File:

bash
Copy code
cp .env.example .env
Generate Application Key:

bash
Copy code
php artisan key:generate
Configure Database:

Open the .env file and update the following lines with your database credentials:
env
Copy code
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_database_user
DB_PASSWORD=your_database_password
Run Database Migrations:

bash
Copy code
php artisan migrate
Usage
Run the Application Locally:
bash
Copy code
php artisan serve
Access the Application:
Open a browser and go to http://localhost:8000.
Deployment with Podman
To deploy this application using Podman containers:

Create a Dockerfile: Ensure there is a Dockerfile in the project root for building the Laravel application.

Create a Podman Compose File: Use podman-compose.yml to configure both the Laravel application and the MySQL container.

Run the Application:

bash
Copy code
podman-compose up -d
Access the Application:

Open a browser and navigate to http://localhost:8000.
