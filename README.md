# 📦 Inventory Management System

<p align="center">
  <img src="https://img.shields.io/badge/CodeIgniter_3-EF4223?style=for-the-badge&logo=codeigniter&logoColor=white"/>
  <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white"/>
  <img src="https://img.shields.io/badge/AdminLTE-00ADB5?style=for-the-badge"/>
</p>

> A web-based Inventory Management System built with **CodeIgniter 3** (PHP MVC framework) that allows users to manage products, brands, and product categories with full CRUD operations, search/filter, and pagination.

---

## 📌 Table of Contents
- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Screenshots](#screenshots)
- [Getting Started](#getting-started)
- [Database Setup](#database-setup)
- [Usage](#usage)

---

## 📖 About

The Inventory Management System is a full-stack web application built using the **CodeIgniter 3 MVC architecture**. It provides an admin dashboard (powered by **AdminLTE**) for managing product inventory — including brands, product categories, and products — with search filters and paginated listings.

The system includes secure login with **password hashing** (`password_verify`), session management, flash messages, and form validation — demonstrating core web development skills with PHP and MySQL.

---

## ✨ Features

### 🔐 Authentication
- User login with email and password
- Secure password verification using PHP `password_verify()`
- Session-based access control
- Flash messages for login errors

### 📊 Dashboard
- Overview statistics (brands, users, visitors, bonus counts)
- AdminLTE sidebar navigation with search

### 🏷️ Brands
- Add, edit, delete, view brands
- Filter brands by name, code, and status
- Paginated brand listing (5 per page)
- Unique code validation

### 📂 Product Categories
- Add, edit, delete, view product categories
- Filter by name, code, and status
- Paginated listing (2 per page)
- Unique code validation

### 📦 Products
- Add, edit, delete, view products
- Linked to brands and product categories
- Filter by name, code, brand, and category
- Paginated listing (2 per page) with DataTables integration
- Product fields: name, code, brand, category, date, description, status

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | CodeIgniter 3 (PHP MVC) |
| Language | PHP 7.x |
| Database | MySQL (`inventory` database, `mysqli` driver) |
| Frontend | Bootstrap 4, AdminLTE, Font Awesome |
| JS Libraries | jQuery 3.7.1, DataTables |
| Server | Apache (XAMPP/WAMP), `.htaccess` routing |

---

## 📂 Project Structure

```
task/
├── application/
│   ├── config/
│   │   ├── database.php        # DB connection (localhost, root, inventory)
│   │   ├── routes.php          # URL routing
│   │   └── autoload.php        # Auto-loaded libraries & helpers
│   ├── controllers/
│   │   ├── Dashboards.php      # Dashboard stats
│   │   ├── Brands.php          # Brand CRUD + filter + pagination
│   │   ├── Product_categories.php  # Category CRUD + filter + pagination
│   │   ├── Products.php        # Product CRUD + filter + pagination
│   │   ├── Logins.php          # Authentication
│   │   ├── Forms.php           # General/information forms
│   │   └── Detail.php          # Detail view controller
│   ├── models/
│   │   ├── Brand_model.php
│   │   ├── Product_model.php
│   │   ├── Product_category_model.php
│   │   ├── Detail_model.php
│   │   └── user_model.php
│   ├── views/
│   │   ├── layouts/
│   │   │   ├── header.php
│   │   │   ├── sidebar.php     # AdminLTE sidebar with nav links
│   │   │   └── footer.php
│   │   ├── brands/             # add, edit, index, view
│   │   ├── product_categories/ # add, edit, index, view
│   │   ├── products/           # add, edit, index, view, detail_view
│   │   └── dashboard.php
│   └── core/
│       ├── MY_Controller.php   # Base controller with layout helper
│       └── MY_Loader.php
├── system/                     # CodeIgniter 3 core
├── .htaccess                   # URL rewriting
└── .gitignore
```

---

## 📸 Screenshots

> _Add screenshots of your dashboard, product listing, and brand management pages here_

<!--
![Dashboard](screenshots/dashboard.png)
![Products](screenshots/products.png)
![Brands](screenshots/brands.png)
-->

---

## ⚙️ Getting Started

### Prerequisites
- [XAMPP](https://www.apachefriends.org/) or WAMP installed
- PHP 7.x
- MySQL 5.7+
- Apache with `mod_rewrite` enabled

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Rifah22/Inventory-Management-System.git
   ```

2. **Move the `task/` folder to your web server root**
   ```bash
   # XAMPP on Windows:
   mv task/ C:/xampp/htdocs/inventory/
   ```

3. **Start Apache and MySQL** in XAMPP Control Panel

4. **Import the database** (see below)

5. **Open in browser**
   ```
   http://localhost/inventory/
   ```

---

## 🗄️ Database Setup

1. Open **phpMyAdmin** → `http://localhost/phpmyadmin`
2. Create a new database named `inventory`
3. Import the SQL file from the repository (if included)
4. The database connection is already configured in `application/config/database.php`:
   ```php
   'hostname' => 'localhost',
   'username' => 'root',
   'password' => '',
   'database' => 'inventory',
   'dbdriver' => 'mysqli',
   ```

### Database Tables

| Table | Description |
|-------|-------------|
| `users` | Stores login credentials (email, hashed password) |
| `brands` | Brand name, code, status |
| `product_categories` | Category name, code, status |
| `products` | Product name, code, brand_id, category_id, date, description, status |

---

## 🧭 Usage

| Module | URL | Features |
|--------|-----|---------|
| Login | `/Forms/general` | Email + password login |
| Dashboard | `/Dashboards/index` | Stats overview |
| Brands | `/brands` | List, add, edit, delete, view |
| Categories | `/product_categories` | List, add, edit, delete, view |
| Products | `/products` | List, add, edit, delete, view with DataTables |

---

## 👩‍💻 Author

**Rifah Sanzida**
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/rifah-sanzida-b58141290/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github)](https://github.com/Rifah22)
