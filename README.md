# 🛒 OnlineShoppingCart

- ##  Description

OnlineShoppingCart is a simple Java-based web application that allows users to browse products, add them to a shopping cart, and proceed to checkout. It demonstrates basic CRUD operations, MVC architecture, and database integration using MySQL.

---
## 🚀 Features

- 🔐  User Registration and Login
- 👁️ View Product List
- 🛒 Add Products to Cart
- ✏️ Update/Delete Items in Cart
- 🔚 Exit
---
 🛠️ Technologies Used

     
- 🖥️ **Java** — A powerful, platform-independent programming language.  
- 🌿 **Hibernate ORM** — Framework for mapping Java objects to database tables.  
- 📦 **Jakarta Persistence API** — API for managing relational data in Java applications.  
- 🛢️ **PostgreSQL** — Advanced open-source relational database system.  
- 🧰 **Maven** — Project management and build automation tool.  
- 🖥️ **Eclipse IDE** — Integrated development environment for Java and other languages.                  
---
##  Maven Dependencies

Add the following to your `pom.xml`:

```xml
<dependencies>
    <dependency>
    <groupId>org.hibernate.orm</groupId>
    <artifactId>hibernate-core</artifactId>
    <version>7.0.6.Final</version>
</dependency>

<dependency>
    <groupId>org.postgresql</groupId>
    <artifactId>postgresql</artifactId>
    <version>42.7.7</version>
</dependency>

    <dependency>
        <groupId>jakarta.persistence</groupId>
        <artifactId>jakarta.persistence-api</artifactId>
        <version>3.2.0</version>
    </dependency>
```
---
## 📁 Project Structure

This Java-based project uses Hibernate ORM with a clean layered architecture.

```plaintext
OnlineShoppingCart/
├── src/
│   └── com/
│       └── onlineshop/
│           ├── App.java                 // Main class with main() method
│           ├── model/
│           │   └── Product.java         // Entity class mapped with Hibernate
│           ├── dao/
│           │   └── ProductDao.java      // Handles database operations
│           └── util/
│               └── HibernateUtil.java   // Provides SessionFactory setup
│
├── resources/
│   └── hibernate.cfg.xml               // Hibernate config file
│   └── log4j.properties                // Logging config (optional)
│
├── pom.xml                             // Maven build configuration
├── README.md                           // Project documentation
└── .gitignore                          // Git ignore rules
yaml
Copy
Edit
```
---


## 📊 Database Table Schema
🔹 Table: products
| Column | Type                 | Description               |
|--------|----------------------|---------------------------|
| id     | SERIAL PRIMARY KEY    | Auto-incremented ID        |
| name   | VARCHAR(100) NOT NULL | Product name               |
| price  | NUMERIC(10, 2) NOT NULL CHECK (price >= 0) | Product price |
---

