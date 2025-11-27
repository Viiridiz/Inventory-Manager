![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white)
![JSP](https://img.shields.io/badge/JSP-007396?style=for-the-badge&logo=java&logoColor=white)
![DAO](https://img.shields.io/badge/Design_Pattern-DAO-blue?style=for-the-badge)

# Depot

A complete web-based inventory and order management system built using Java Servlets, JSP, and the DAO pattern. This system allows businesses to manage products, suppliers, stock levels, and orders, while also generating downloadable inventory reports.

## Features Overview

### Product Management
- Add new products with SKU, category, price, and description
- Edit or delete existing products
- Update stock quantities
- Track product information across the system

### Supplier Management
- Add and manage supplier information
- Store supplier contact details (phone and email)
- Delete suppliers when no longer needed

### Order Management
- Place new orders with supplier and product selection
- Automatic stock level adjustments when orders are completed
- View and manage order history
- Track order status and dates

### Reporting
- Generate downloadable `.txt` inventory reports
- View current stock levels and system summaries
- Access system information including total products and suppliers

### User Interface
- Clean, responsive dashboard
- Toast notifications for user feedback
- Intuitive forms and data tables
- Modern design with easy navigation

## Architecture

The system follows a multi-tier architecture pattern:

- **Presentation Layer**: JSP pages for user interface
- **Business Logic Layer**: Java Servlets for request handling
- **Data Access Layer**: DAO pattern for database operations
- **Database Layer**: MySQL for data persistence

This separation of concerns makes the application maintainable, testable, and scalable.

## Screenshots

### Inventory Dashboard
![Inventory Dashboard](screenshots/inventory-dashboard.png)

View system information including total products and suppliers, and generate inventory reports.

### Order Management
![Order Management](screenshots/order-management.png)

Track existing orders with details including supplier, products ordered, status, and order dates.

### Product Catalog
![Product Catalog](screenshots/product-catalog.png)

Browse available products and place new orders with supplier and product selection.

### Supplier and Product Management
![Supplier and Product Management](screenshots/supplier-product-management.png)

Manage suppliers with contact information and view the complete product inventory with stock quantities.

### Add/Update Features
![Add Update Features](screenshots/add-update-features.png)

Add new products and suppliers, or update stock levels for existing products.

## Technology Stack

**Backend:**
- Java Servlet API
- DAO Pattern for data access
- JDBC for database connectivity

**Frontend:**
- JSP (JavaServer Pages)
- HTML5
- CSS3
- JavaScript

**Database:**
- MySQL (or compatible SQL database)

**Application Server:**
- Apache Tomcat

## Installation & Setup

### Prerequisites
- JDK 8 or higher
- Apache Tomcat 8.5 or higher
- MySQL 5.7 or higher
- Maven (optional, for dependency management)

### Steps

1. **Clone the repository**
```bash
   git clone https://github.com/Rafat-i/inventory-manager.git
   cd inventory-manager
```

2. **Configure the Database**
   - Create a new database:
```sql
     CREATE DATABASE inventory_db;
```
- Run the `SchemaInitializer` class to initialize the database schema
- Update database credentials in `DbUtil.java`:
```java
     private static final String URL = "jdbc:mysql://localhost:3306/inventory_db";
     private static final String USER = "root";
     private static final String PASSWORD = "your_password";
```

3. **Build the Project**
   - If using Maven:
```bash
     mvn clean package
```
- If building manually, compile all Java files and create a WAR file

4. **Deploy to Tomcat**
   - Copy the generated `.war` file to Tomcat's `webapps/` directory
   - Start Tomcat server:
```bash
     # On Windows
     catalina.bat start
     
     # On Linux/Mac
     ./catalina.sh start
```

5. **Access the Application**
```
   http://localhost:8080/inventory-manager
```

## Project Structure
```
inventory-manager/
├── src/
│   └── main/
│       └── java/
│           └── com.example.inventory_manager/
│               ├── controller/              # Servlet controllers
│               │   ├── InventoryServlet.java
│               │   └── OrderServlet.java
│               ├── dao/                     # Data Access Layer
│               │   └── impl/
│               │       ├── InventoryItemDAO.java
│               │       ├── OrderDAO.java
│               │       ├── ProductDAO.java
│               │       └── SupplierDAO.java
│               ├── db/                      # Database utilities
│               │   ├── DAOTestMain.java
│               │   ├── DbTestMain.java
│               │   ├── DbUtil.java
│               │   ├── Main.java
│               │   └── SchemaInitializer.java
│               └── model/                   # Data models
│                   ├── InventoryItem.java
│                   ├── InventoryManager.java
│                   ├── InventoryReport.java
│                   ├── Main.java
│                   ├── Order.java
│                   ├── Product.java
│                   ├── Report.java (interface)
│                   ├── ReportGeneratable.java (interface)
│                   ├── StockTrackable.java (interface)
│                   └── Supplier.java
├── src/
│   └── main/
│       ├── resources/                       # Resource files
│       └── webapp/                          # Web application files
│           ├── WEB-INF/
│           │   └── web.xml
│           ├── index.jsp
│           ├── inventory.jsp
│           └── orders.jsp
├── target/                                  # Build output directory
├── screenshots/                             # Application screenshots
├── .gitignore
├── mvnw                                     # Maven wrapper (Unix)
├── mvnw.cmd                                 # Maven wrapper (Windows)
├── pom.xml                                  # Maven configuration
└── README.md
```

## Usage

### Managing Products
1. Navigate to the Inventory tab
2. Scroll to "Add New Product" section
3. Fill in product details (name, SKU, category, price, quantity, description)
4. Click "Add Product"

### Managing Suppliers
1. Navigate to the Inventory tab
2. Scroll to "Add New Supplier" section
3. Enter supplier information (name, email, phone)
4. Click "Add Supplier"

### Placing Orders
1. Navigate to the Orders tab
2. Scroll to "Place a New Order" section
3. Select a supplier from the dropdown
4. Select a product by SKU
5. Enter quantity
6. Click "Place Order"

### Updating Stock
1. Navigate to the Inventory tab
2. Go to "Update Stock" section
3. Select product by SKU
4. Enter quantity change (use + for increase, - for decrease)
5. Click "Update Stock"

### Generating Reports
1. Navigate to the Inventory tab
2. Click "Generate Inventory Report"
3. Report will download as a `.txt` file

## Future Improvements

### Security
- User authentication and authorization
- Role-based access control (Admin, Manager, Viewer)
- Password encryption
- Session management

### Features
- Advanced search and filtering
- Pagination for large datasets
- Barcode scanning support
- Low stock alerts and notifications
- Order tracking and status updates
- Supplier performance analytics

### Reporting
- Export reports as PDF and Excel
- Customizable report templates
- Scheduled automatic reports
- Data visualization with charts and graphs

### Technical
- REST API for third-party integrations
- Mobile-responsive design improvements
- Real-time updates using WebSockets
- Caching for improved performance
- Unit and integration tests
