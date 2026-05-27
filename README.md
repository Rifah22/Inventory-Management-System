# 📦 Inventory Management System

<p align="center">
  <img src="https://img.shields.io/badge/CodeIgniter-EF4223?style=for-the-badge&logo=codeigniter&logoColor=white"/>
  <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white"/>
</p>

> A full-featured inventory and stock management web application built with CodeIgniter 3, enabling businesses to track products, manage stock levels, and generate reports.

---

## 📌 Table of Contents
- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Screenshots](#screenshots)
- [Getting Started](#getting-started)
- [Database Setup](#database-setup)

---

## 📖 About

The Inventory Management System is a web-based application that helps businesses manage their product stock efficiently. Built using the **CodeIgniter 3** PHP framework and following the MVC architecture, it provides a clean admin dashboard to handle product entries, stock updates, and reporting.

This project demonstrates knowledge of MVC design patterns, RESTful routing, form validation, and database-driven web development.

---

## ✨ Features

- 🔐 Secure admin login & session management
- 📦 Add, edit, delete product records
- 📊 Real-time stock level tracking
- 🔔 Low-stock alerts
- 🏷️ Category management
- 🧾 Purchase and sales tracking
- 📈 Report generation (stock summary, transaction history)
- 👤 User role management

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | CodeIgniter 3 (PHP MVC) |
| Frontend | HTML5, CSS3, Bootstrap, JavaScript |
| Database | MySQL |
| Server | Apache (XAMPP/WAMP) |

---

## 📸 Screenshots

> _Add screenshots of your dashboard, product list, and reports here_

<!--
![Dashboard](screenshots/dashboard.png)
![Product List](screenshots/products.png)
![Reports](screenshots/reports.png)
-->

---

## ⚙️ Getting Started

### Prerequisites
- XAMPP or WAMP
- PHP 7.x
- MySQL 5.7+
- Composer (optional)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Rifah22/Inventory-Management-System.git
   ```

2. **Move to your web server root**
   ```bash
   # XAMPP:
   mv Inventory-Management-System /xampp/htdocs/
   ```

3. **Set base URL** in `application/config/config.php`:
   ```php
   $config['base_url'] = 'http://localhost/Inventory-Management-System/';
   ```

4. **Configure database** in `application/config/database.php`:
   ```php
   $db['default'] = array(
       'hostname' => 'localhost',
       'username' => 'root',
       'password' => '',
       'database' => 'inventory_db',
   );
   ```

5. **Import the database** (see below)

6. **Run the app**
   ```
   http://localhost/Inventory-Management-System/
   ```

---

## 🗄️ Database Setup

1. Open **phpMyAdmin** → Create database `inventory_db`
2. Import the `.sql` file from the repository
3. Default admin credentials (update after first login):
   ```
   Username: admin
   Password: admin123
   ```

---

## 📂 Project Structure (CodeIgniter MVC)

```
Inventory-Management-System/
├── application/
│   ├── controllers/    # Business logic
│   ├── models/         # Database queries
│   ├── views/          # UI templates
│   └── config/         # App configuration
├── assets/             # CSS, JS, images
└── index.php
```

---

## 👩‍💻 Author

**Rifah Sanzida**  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/rifah-sanzida-b58141290/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github)](https://github.com/Rifah22)
