# 📚 DigiBook

<p align="center">
  <b>A Persian Online Bookstore built with PHP & MySQL</b>
</p>

<p align="center">
  🎓 University Project &nbsp;•&nbsp;
  🤖 AI-Assisted Development &nbsp;•&nbsp;
  🌐 Live Demo
</p>

<p align="center">
  <a href="https://digibookdb.freedev.app/">
    <img src="https://img.shields.io/badge/🌐_Live_Demo-DigiBook-7c6bff?style=for-the-badge" alt="Live Demo"/>
  </a>
  <a href="https://github.com/hemloblack/digibook">
    <img src="https://img.shields.io/badge/💻_Source_Code-GitHub-181717?style=for-the-badge&logo=github" alt="GitHub"/>
  </a>
</p>

---

## 📝 About The Project

**DigiBook** is a Persian online bookstore created as a **university project**.

The project was developed as a practical example of building a database-driven web application with **PHP, MySQL/MariaDB, HTML, CSS and JavaScript**.

The project includes a complete basic shopping flow:

**Browse Books → View Details → Add to Cart → Checkout → Create Order**

It also includes user authentication, phone-based OTP verification and an administrator role for managing books.

> 🤖 AI tools were used as part of the development process to assist with implementation, debugging and UI development.

---

## ✨ Features

### 📚 Bookstore

* 📖 Browse available books
* 🔎 View individual book details
* 🏷️ Book categories
* ✍️ Author information
* 💰 Price display
* 🖼️ Book cover images
* 📱 Responsive layout

### 🛒 Shopping Cart

* ➕ Add books to cart
* ➖ Increase/decrease quantity
* 🗑️ Remove books
* 💰 Automatic total calculation
* 💾 Client-side cart persistence using `localStorage`

### 👤 Authentication

* 🔐 User login
* 📝 User registration
* 📱 Phone number verification
* 🔢 6-digit OTP verification
* 🔒 Password hashing
* 🧑 User roles
* 👑 Administrator role
* 🚪 Logout
* 🔄 Session management

### 📦 Checkout & Orders

* 📝 Customer information form
* 📧 Email collection
* 📍 Address collection
* 💰 Automatic order total
* 🧾 Order creation
* 📦 Order item storage
* ✅ Order confirmation

### 👑 Admin

* ➕ Add new books
* 🖼️ Upload book images
* 🏷️ Select book category
* 💰 Set book price
* ✍️ Add author information
* 📝 Add book description
* 🔐 Admin-only access

---

## 🛠️ Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=php,mysql,html,css,js,git,github,vscode&perline=8" />
</p>

### Backend

* 🐘 PHP
* 🔌 PDO
* 🔐 PHP Sessions
* 🔑 Password Hashing

### Database

* 🐬 MySQL / MariaDB
* 🗃️ SQL
* 🔗 Relational Database
* 🔒 Prepared Statements

### Frontend

* 🌐 HTML5
* 🎨 CSS3
* ⚡ JavaScript
* 💾 LocalStorage
* 📱 Responsive Design
* 🔄 RTL / Persian UI

### External Services

* 📱 SMS.ir API
* 🔤 Google Fonts — Vazirmatn

---

## 🏗️ Project Structure

```text
digibook/
│
├── admin/
│   └── add-book.php
│
├── assets/
│   ├── css/
│   │   └── style.css
│   │
│   └── js/
│       └── script.js
│
├── config/
│   └── database.php
│
├── includes/
│   ├── auth.php
│   ├── footer.php
│   ├── header.php
│   └── otp_helper.php
│
├── uploads/
│
├── auth_tables.sql
├── bookstore_db.sql
├── init_db.sql
│
├── index.php
├── book.php
├── cart.php
├── checkout.php
├── login.php
├── register.php
└── logout.php
```

---

## 🔐 Authentication Flow

The registration process is implemented as a multi-step flow:

```text
📱 Enter Phone Number
        ↓
📨 Send OTP
        ↓
🔢 Verify 6-Digit Code
        ↓
👤 Enter Account Information
        ↓
🔒 Hash Password
        ↓
✅ Create Account
        ↓
🚀 Login Session
```

OTP codes are stored in the database with an expiration time and marked as used after successful verification.

The project also contains a development fallback when SMS delivery is unavailable.

---

## 🗄️ Database

The project uses a relational database with tables for:

| Table         | Purpose                    |
| ------------- | -------------------------- |
| `books`       | 📚 Book information        |
| `users`       | 👤 User accounts           |
| `otp_codes`   | 🔢 OTP verification        |
| `orders`      | 📦 Customer orders         |
| `order_items` | 🛒 Items inside each order |

The order system connects orders with their individual books through relational keys.

---

## 🎨 UI / Design

DigiBook uses a custom dark-themed interface designed specifically for the Persian language.

### Design Highlights

* 🌙 Dark UI
* 💜 Purple / Blue gradient color palette
* ✨ Glass-like effects
* 🎴 Book cards
* 🖱️ Hover animations
* 📱 Responsive layout
* 🇮🇷 Persian RTL interface
* 🔤 Vazirmatn typography
* 🔔 JavaScript notifications
* ⬆️ Scroll-to-top button

The main stylesheet defines the project's color system, shadows, gradients, cards, navigation, forms and responsive behavior.

---

## 🛒 Shopping Flow

```text
📚 Browse Books
      ↓
📖 View Book
      ↓
🛒 Add to Cart
      ↓
🛍️ Manage Cart
      ↓
📝 Enter Customer Information
      ↓
📦 Create Order
      ↓
✅ Order Confirmation
```

The cart is handled on the client side using JavaScript and `localStorage`, while completed orders are stored in the database.

---

## 📸 Live Demo

🌐 **Try DigiBook:**

https://digibookdb.freedev.app/

> ⚠️ This is a demonstration/academic project and is not intended to be used as a production e-commerce platform.

---

## 🚀 Running Locally

### 1️⃣ Clone the repository

```bash
git clone https://github.com/hemloblack/digibook.git
cd digibook
```

### 2️⃣ Setup the database

Create a MySQL/MariaDB database and import:

```text
bookstore_db.sql
auth_tables.sql
init_db.sql
```

### 3️⃣ Configure the database

Update your database credentials in:

```text
config/database.php
```

### 4️⃣ Configure the web server

Place the project inside your PHP server directory, for example:

```text
htdocs/digibook
```

Then open:

```text
http://localhost/digibook/
```

---

## 📌 Project Status

🟢 **Completed — Academic Project**

This project was created primarily as a university assignment and as a practical exercise in building a complete database-driven web application.

Future improvements could include:

* 💳 Real payment gateway integration
* 📦 Advanced order management
* 🔍 Book search & filtering
* ⭐ Reviews and ratings
* ❤️ Wishlist
* 📊 Advanced admin dashboard
* 🔐 Stronger production security
* ⚡ Performance optimization

---

## 👨‍💻 Author

**Hamidreza**

🎓 Software Engineering Student
🐍 Python & Backend Development
💻 Web Development

<p align="center">
  <a href="https://github.com/hemloblack">
    <img src="https://img.shields.io/badge/GitHub-hemloblack-181717?style=for-the-badge&logo=github" />
  </a>
</p>

---

<p align="center">
  ⭐ If you found this project interesting, consider giving it a star!
</p>
