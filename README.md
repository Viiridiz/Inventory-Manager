#  inventory-management-system

![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white)
![JSP](https://img.shields.io/badge/JSP-007396?style=for-the-badge&logo=java&logoColor=white)
![DAO](https://img.shields.io/badge/Design_Pattern-DAO-blue?style=for-the-badge)

A web-based inventory management application developed in Java using Servlets, JSP, and the DAO pattern.

## About This Project

> This project is a dynamic, web-based inventory management application. It allows users to manage products, track suppliers, and process orders from placement to completion. It also features the ability to generate downloadable inventory reports, providing a complete solution for basic inventory needs.

## Key Features

* **Product Management:** Add new products, delete existing ones, and update stock quantities.
* **Supplier Management:** Maintain a complete list of suppliers, including adding and deleting supplier records.
* **Full Order Lifecycle:**
    * **Place Orders:** Create new orders by selecting a supplier, choosing products, and setting quantities.
    * **Complete Orders:** Mark orders as 'completed', which automatically updates the inventory stock levels.
* **Reporting:** Generate and download a `.txt` file of the current inventory report at any time.
* **Modern UI/UX:**
    * A dynamic web interface built with **JSP (JavaServer Pages)**.
    * **Toast messages** provide non-intrusive feedback for user actions (e.g., "Order placed successfully!").
* **Robust Backend:** Utilizes the **DAO (Data Access Objects) pattern** for clean, maintainable, and decoupled database interaction.

## 🛠️ Technology Stack

* **Backend:** Java (Servlets)
* **Frontend:** JSP (JavaServer Pages), HTML, CSS, JavaScript (for Toasts)
* **Database:** *[Specify your database, e.g., MySQL, PostgreSQL]*
* **Web Server:** Apache Tomcat
* **Design Pattern:** DAO (Data Access Object)

## 🏁 Getting Started

Follow these instructions to get a local copy up and running.

### Prerequisites

* Java JDK (e.g., JDK 11 or 17)
* Apache Tomcat (e.g., v9.0)
* A SQL Database (e.g., MySQL Server)
* An IDE (e.g., IntelliJ IDEA, Eclipse)
* [Optional: Apache Maven]

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    ```
2.  **Database Setup:**
    * Create a new database (e.g., `inventory_db`).
    * Import the database schema from the `.sql` file provided in the repo.
    * Update the database connection details (URL, username, password) in the `DAO` or `DBConnection` utility class.
3.  **Configure Tomcat:**
    * Add your Apache Tomcat server to your IDE.
    * Build the project (e.g., `mvn clean install` if using Maven) to produce a `.war` file.
4.  **Deploy:**
    * Deploy the `.war` file to your Tomcat server.
    * Start the server.
5.  **Access the application:**
    * Open your browser and navigate to `http://localhost:8080/your-app-context-path`

