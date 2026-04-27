# 🏢 Web Based Apartment Sales System

A Java Servlet + JSP web application for managing apartment sales, bookings, payments, and reviews. Supports three user roles: **Buyer**, **Seller**, and **Admin**.

---

## Features

**Buyers** — Browse apartments, save favourites, book, pay, and review  
**Sellers** — Add/edit/delete listings, manage bookings and payments  
**Admins** — Manage users, apartments, reviews, reports, settings, and FAQs

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Java Servlets |
| Frontend | JSP, HTML, CSS, JavaScript |
| Database | Microsoft SQL Server |
| Build | Maven |
| Server | Apache Tomcat 9 |
| Architecture | MVC (Servlet → Service → DAO) |

---

## Prerequisites

| Tool | Version | Verify |
|---|---|---|
| Java JDK | 16+ | `java -version` |
| Maven | Any | `mvn -version` |
| Apache Tomcat | **9** (required — uses `javax.servlet`) | — |
| Microsoft SQL Server | Developer / Express Edition | — |
| SQL Server Management Studio or Azure Data Studio | Any | — |
| IntelliJ IDEA | Ultimate recommended | — |

---

## Setup & Run

### 1. Clone the repo

```bash
git clone https://github.com/Himaka12/WebBasedApartmentSalesSystem.git
cd WebBasedApartmentSalesSystem
```

---

### 2. Open in IntelliJ IDEA

1. **File → Open** → select the `WebBasedApartmentSalesSystem` folder
2. Wait for indexing to complete
3. IntelliJ will detect the Maven project automatically

---

### 3. Load Maven dependencies

Right-click `pom.xml` → **Maven → Reload Project**

Or via terminal:
```bash
mvn clean package
```

---

### 4. Create the database

Open SQL Server Management Studio (or Azure Data Studio) and run:

```sql
CREATE DATABASE Apartment_06;
GO
```

Then open `src/main/resources/schema.sql` and run the **full script** inside the `Apartment_06` database.

This creates all tables, indexes, constraints, a default admin account, and sample FAQ records.

---

### 5. Configure the database connection

Open `src/main/java/com/project/util/DBUtil.java` and update:

```java
private static final String URL = "jdbc:sqlserver://localhost:1433;databaseName=Apartment_06;encrypt=true;trustServerCertificate=true";
private static final String USERNAME = "sa";
private static final String PASSWORD = "your_password_here";
```

Make sure:
- SQL Server is **running**
- **TCP/IP is enabled** (SQL Server Configuration Manager → Protocols → TCP/IP → Enabled)
- **SQL Server Authentication** is enabled (not Windows-only)
- Port `1433` is active
- The database name is exactly `Apartment_06`

---

### 6. Configure Tomcat in IntelliJ

1. **Run → Edit Configurations → + → Tomcat Server → Local**
2. Set your Tomcat 9 installation directory
3. Go to the **Deployment** tab → **+ → Artifact** → select the **WAR exploded** artifact
4. Set **Application context** to `/Apartment06`
5. Click **Apply → OK**

---

### 7. Run

Click the green **Run** button. Once Tomcat starts, open:

```
http://localhost:8080/Apartment06/
```

---

## Default Admin Login

| Field | Value |
|---|---|
| Email | admin@apartmentx.com |
| Password | admin123 |

Admin login page:
```
http://localhost:8080/Apartment06/adminlogin.jsp
```

> If login fails, confirm the `admins` table has data after running `schema.sql`.

---

## Project Structure

```
src/main/
├── java/com/project/
│   ├── DAO/        # Database operations
│   ├── model/      # Data objects (User, Apartment, Booking, Payment...)
│   ├── service/    # Business logic
│   ├── servlet/    # HTTP request handlers
│   ├── strategy/   # Payment strategies (Advance, Half, Installment)
│   └── util/       # DB connection, password, validation helpers
├── resources/
│   └── schema.sql  # Full database setup script
└── webapp/
    ├── WEB-INF/
    ├── css/ & js/
    └── *.jsp       # All UI pages
```

---

## Common Issues

| Problem | Fix |
|---|---|
| Maven deps not loading | Right-click `pom.xml` → Maven → Reload Project |
| Tomcat won't start | Check port 8080 is free; confirm Tomcat 9 is selected |
| 404 Not Found | Confirm context path is `/Apartment06` |
| Database connection failed | Check `DBUtil.java` credentials; verify SQL Server is running on port 1433 with TCP/IP enabled |
| Login not working | Confirm `schema.sql` was run and user/admin records exist in the DB |
| SQL script errors | Make sure you're running on **SQL Server**, not MySQL — the script uses `NVARCHAR`, `GO`, `SEQUENCE`, `SYSUTCDATETIME()` |

---

## Author

**Himaka Uthpala** — [github.com/Himaka12](https://github.com/Himaka12)
