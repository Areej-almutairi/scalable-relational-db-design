# Enterprise-Grade Relational Database Design (Scalable Micro-Blogging Architecture)

##  Project Overview
This project features the design and implementation of a robust, fully relational database system built using MySQL, simulated for micro-blogging platforms (similar to Twitter). It showcases advanced relational modeling, optimized transactional flows, foreign key constraints, and secure user data management utilizing programmatic stored procedures and hashing concepts.

---

##  Tech Stack & Tools Used
* **Database Engine:** MySQL Server
* **Design Tool:** MySQL Workbench (EER Diagram & Modeling)
* **Language:** SQL (Structured Query Language)

---

##  Database Architecture & ER Diagram
The system is architected around a normalized relational model designed to handle heavy write and read operations across core social entities.

* **Core Tables:**
  * `Users` ➔ Manages unique identities, secure credentials, and creation timestamps.
  * `Tweets` ➔ Stores core micro-blog posts linked directly to their respective authors via strict foreign keys.
  * `Likes` ➔ A many-to-many junction table managing the interaction network between users and specific content.
  * `Follows` ➔ A self-referencing relationship mapping complex user-to-user networks (Followers/Following).

---

##  Key Database Features
* **Referential Integrity:** Enforced cascading constraints across relationships (`1:N` and `M:M`) to ensure structural data persistence.
* **Automated Logic:** Leveraged internal MySQL functions to auto-generate transactional timestamps upon user creation and tweeting activities.
* **Procedural Security:** Developed specialized **Stored Procedures** (e.g., `createUser`) to wrap insertions into the system safely, demonstrating programmatic execution layer design.

---

##  System Schema & Implementation Preview

###  Entity-Relationship (ER) Diagram
*The relational mapping exhibiting structural optimization and table connections.*
![ER Diagram](screenshots/er_diagram.png)

###  User Records & Transactions
*Granular view of the generated schema testing user registration datasets.*
![Users Table](screenshots/users_table.png)

###  Executing Stored Procedures
*Live demonstration of executing operational queries inside MySQL Workbench.*
![Procedure Execution](screenshots/stored_procedure.png)

---

##  Author
* **Areej Abdulrahman Al-Mutairi**
* **Role:** Data Analyst & Business Intelligence Professional