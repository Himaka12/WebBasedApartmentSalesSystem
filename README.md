# 🏢 Web Based Apartment Sales System

A Java Servlet and JSP based web application for managing apartment sales, apartment listings, bookings, payments, favourites, reviews, users, sellers, buyers, administrators, and FAQ management.

The system is designed as a complete apartment marketplace platform where buyers can browse apartments, book apartments, manage favourites, make payments, and submit reviews, while sellers can manage apartment listings and booking requests. Administrators can manage users, apartments, reviews, reports, settings, and overall system operations.

---

## 📌 Project Overview

The **Web Based Apartment Sales System** is a full-stack Java web application developed to simplify apartment sales and property management through a browser-based platform.

The application supports three main user areas:

- **Buyers** can browse apartments, view details, save favourites, make bookings, manage cards, make payments, and submit reviews.
- **Sellers** can add apartments, manage apartment listings, view buyer bookings, and track payments.
- **Admins** can manage users, apartments, reviews, reports, system settings, and administrator accounts.

This project uses a layered Java architecture with JSP pages for the frontend, Servlets for request handling, service classes for business logic, DAO classes for database operations, and Microsoft SQL Server for data storage.

---

## ✨ Key Features

- Buyer registration and login
- Seller registration and login
- Admin login and admin dashboard
- Apartment listing management
- Add, edit, delete, and view apartments
- Apartment image handling
- Apartment search and browsing
- Apartment detail view
- Buyer favourites management
- Apartment booking system
- Seller booking management
- Buyer booking management
- Buyer card management
- Payment handling
- Multiple payment strategies
- Buyer review management
- Admin review management
- FAQ management
- Admin user management
- Admin apartment management
- Admin reports section
- Admin settings section
- Profile update and delete functionality
- SQL Server database integration
- Maven based WAR project structure

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | Java Servlets |
| Frontend | JSP, HTML, CSS, JavaScript |
| Database | Microsoft SQL Server |
| Build Tool | Maven |
| Server | Apache Tomcat |
| JDBC Driver | Microsoft SQL Server JDBC |
| Architecture | MVC-style layered architecture |
| IDE Recommended | IntelliJ IDEA |

---

## 📁 Project Structure

    WebBasedApartmentSalesSystem/
    │
    ├── src/
    │   └── main/
    │       │
    │       ├── java/
    │       │   └── com/
    │       │       └── project/
    │       │           │
    │       │           ├── DAO/
    │       │           │   ├── AdminDAO.java
    │       │           │   ├── ApartmentDAO.java
    │       │           │   ├── BookingDAO.java
    │       │           │   ├── BuyerCardDAO.java
    │       │           │   ├── FAQDAO.java
    │       │           │   ├── FavouriteDAO.java
    │       │           │   ├── PaymentDAO.java
    │       │           │   ├── ReviewDAO.java
    │       │           │   └── UserDAO.java
    │       │           │
    │       │           ├── model/
    │       │           │   ├── Admin.java
    │       │           │   ├── Apartment.java
    │       │           │   ├── ApartmentImage.java
    │       │           │   ├── Booking.java
    │       │           │   ├── Buyer.java
    │       │           │   ├── BuyerCard.java
    │       │           │   ├── FAQ.java
    │       │           │   ├── Favourite.java
    │       │           │   ├── Payment.java
    │       │           │   ├── Review.java
    │       │           │   ├── Seller.java
    │       │           │   └── User.java
    │       │           │
    │       │           ├── service/
    │       │           │   ├── ApartmentService.java
    │       │           │   ├── BookingService.java
    │       │           │   ├── BuyerCardService.java
    │       │           │   ├── FAQService.java
    │       │           │   ├── FavouriteService.java
    │       │           │   ├── PaymentService.java
    │       │           │   └── UserService.java
    │       │           │
    │       │           ├── servlet/
    │       │           │   ├── AddApartmentServlet.java
    │       │           │   ├── AdminApartmentManagementServlet.java
    │       │           │   ├── AdminDashboardServlet.java
    │       │           │   ├── AdminLoginServlet.java
    │       │           │   ├── AdminManagementServlet.java
    │       │           │   ├── AdminRegistrationServlet.java
    │       │           │   ├── AdminReportsServlet.java
    │       │           │   ├── AdminReviewManagementServlet.java
    │       │           │   ├── AdminSettingsServlet.java
    │       │           │   ├── AdminUserManagementServlet.java
    │       │           │   ├── AllApartmentsServlet.java
    │       │           │   ├── BookingFormServlet.java
    │       │           │   ├── BookingServlet.java
    │       │           │   ├── BuyerBookingsServlet.java
    │       │           │   ├── BuyerCardServlet.java
    │       │           │   ├── BuyerDashboardServlet.java
    │       │           │   ├── BuyerFavouritesServlet.java
    │       │           │   ├── BuyerPaymentsServlet.java
    │       │           │   ├── BuyerReviewServlet.java
    │       │           │   ├── DeleteApartmentServlet.java
    │       │           │   ├── DeleteProfileServlet.java
    │       │           │   ├── EditApartmentServlet.java
    │       │           │   ├── FAQServlet.java
    │       │           │   ├── FavouriteServlet.java
    │       │           │   ├── ImageDisplayServlet.java
    │       │           │   ├── ListApartmentsServlet.java
    │       │           │   ├── LoginServlet.java
    │       │           │   ├── LogoutServlet.java
    │       │           │   ├── MyApartmentsServlet.java
    │       │           │   ├── PaymentServlet.java
    │       │           │   ├── RegisterServlet.java
    │       │           │   ├── ReviewServlet.java
    │       │           │   ├── ReviewsServlet.java
    │       │           │   ├── SellerBookingsServlet.java
    │       │           │   ├── SellerDashboardServlet.java
    │       │           │   ├── SellerPaymentsServlet.java
    │       │           │   ├── SetupApartmentDataServlet.java
    │       │           │   ├── UpdateProfileServlet.java
    │       │           │   └── ViewApartmentServlet.java
    │       │           │
    │       │           ├── strategy/
    │       │           │   ├── AdvancePaymentStrategy.java
    │       │           │   ├── HalfPaymentStrategy.java
    │       │           │   ├── InstallmentPaymentStrategy.java
    │       │           │   ├── PaymentStrategy.java
    │       │           │   └── PaymentStrategyFactory.java
    │       │           │
    │       │           └── util/
    │       │               ├── DBUtil.java
    │       │               ├── PasswordMigrationUtil.java
    │       │               ├── PasswordUtil.java
    │       │               ├── TestSQLServer.java
    │       │               └── ValidationUtil.java
    │       │
    │       ├── resources/
    │       │   └── schema.sql
    │       │
    │       └── webapp/
    │           ├── WEB-INF/
    │           ├── css/
    │           ├── includes/
    │           ├── js/
    │           ├── resources/images/
    │           ├── index.jsp
    │           ├── login.jsp
    │           ├── register.jsp
    │           ├── apartments.jsp
    │           ├── apartmentdetail.jsp
    │           ├── addapartment.jsp
    │           ├── editapartment.jsp
    │           ├── myapartments.jsp
    │           ├── bookingform.jsp
    │           ├── buyerbookings.jsp
    │           ├── sellerbookings.jsp
    │           ├── buyerdashboard.jsp
    │           ├── sellerdashboard.jsp
    │           ├── buyerfavourites.jsp
    │           ├── buyerpayments.jsp
    │           ├── sellerpayments.jsp
    │           ├── reviews.jsp
    │           ├── addreview.jsp
    │           ├── adminlogin.jsp
    │           ├── admindashboard.jsp
    │           ├── adminapartmentmanagement.jsp
    │           ├── adminusermanagement.jsp
    │           ├── adminreviewmanagement.jsp
    │           ├── adminreports.jsp
    │           ├── adminsettings.jsp
    │           ├── faq.jsp
    │           ├── contact.jsp
    │           └── about.jsp
    │
    ├── pom.xml
    ├── README.md
    └── .gitignore

---

## 🗄️ Database Overview

The project uses **Microsoft SQL Server** as the database.

The database setup script is located at:

    src/main/resources/schema.sql

The schema includes the following main tables:

| Table | Purpose |
|---|---|
| users | Stores buyer and seller login/profile data |
| buyers | Stores buyer-specific details |
| sellers | Stores seller-specific details |
| apartments | Stores apartment listings |
| apartment_images | Stores apartment image records |
| favourites | Stores buyer favourite apartments |
| bookings | Stores apartment booking records |
| buyerCards | Stores buyer card details |
| payments | Stores apartment payment records |
| reviews | Stores buyer reviews |
| admins | Stores administrator accounts |
| faqs | Stores FAQ records |

The script also creates sequences, primary keys, foreign keys, constraints, indexes, sample admin data, and sample FAQ records.

---

## 🧩 Main System Modules

### Buyer Module

The buyer module allows registered buyers to:

- Login and access buyer dashboard
- Browse apartment listings
- View apartment details
- Add apartments to favourites
- Create apartment bookings
- Manage bookings
- Add and manage card details
- Make payments
- Submit and manage reviews
- Update or delete profile

---

### Seller Module

The seller module allows registered sellers to:

- Login and access seller dashboard
- Add new apartment listings
- Upload apartment information
- Edit existing apartment details
- Delete apartment listings
- View seller apartments
- Manage buyer booking requests
- View payment records

---

### Admin Module

The admin module allows administrators to:

- Login to admin dashboard
- Manage apartments
- Manage users
- Manage reviews
- Manage admin accounts
- View system reports
- Manage settings
- Monitor platform activity

---

### Apartment Module

The apartment module manages:

- Apartment title
- Apartment description
- Address and city
- State and postal code
- Contact number
- Property type
- Price
- Bedrooms
- Bathrooms
- Area in square feet
- Availability status
- Apartment images

---

### Booking Module

The booking module manages:

- Buyer booking requests
- Seller booking visibility
- Booking date and time
- Booking messages
- Booking status such as Pending, Confirmed, Cancelled, and Completed

---

### Payment Module

The payment module manages apartment-related payments using different payment strategy classes.

Supported payment types include:

- Advance Payment
- Half Payment
- Installment Payment

---

### Review Module

The review module allows buyers to add feedback with:

- Rating
- Review title
- Review text
- Visibility status

Admins can manage reviews through the admin review management section.

---

### FAQ Module

The FAQ module stores common questions and answers related to registration, booking, payment, account management, general information, and support.

---

## 🏗️ Application Architecture

The project follows a layered architecture:

    JSP Pages
        ↓
    Servlets
        ↓
    Services
        ↓
    DAO Classes
        ↓
    SQL Server Database

### Layer Responsibilities

| Layer | Responsibility |
|---|---|
| JSP | Displays UI pages to users |
| Servlet | Handles HTTP requests and responses |
| Service | Contains business logic |
| DAO | Handles database operations |
| Model | Represents system data objects |
| Utility | Provides database, password, and validation helpers |

---

## ✅ Prerequisites

Before running this project, install the following software:

### 1. Java JDK

Install **Java JDK 16 or higher**.

Check installation:

    java -version

The project is configured with Maven compiler source and target version 16.

---

### 2. Maven

Install Maven or use the Maven support included in IntelliJ IDEA.

Check installation:

    mvn -version

---

### 3. Apache Tomcat

Install **Apache Tomcat 9**.

Tomcat 9 is recommended because this project uses `javax.servlet`, not `jakarta.servlet`.

---

### 4. Microsoft SQL Server

Install Microsoft SQL Server.

You can use:

- SQL Server Developer Edition
- SQL Server Express Edition

Also install one database management tool:

- SQL Server Management Studio
- Azure Data Studio

---

### 5. IntelliJ IDEA

Recommended IDE:

- IntelliJ IDEA Ultimate

You can also use another Java IDE that supports Maven and Tomcat.

---

## 🚀 Setup Instructions

Follow these steps carefully to run the project successfully.

---

## 1. Clone the Repository

Open terminal or command prompt and run:

    git clone https://github.com/Himaka12/WebBasedApartmentSalesSystem.git

Go into the project folder:

    cd WebBasedApartmentSalesSystem

---

## 2. Open the Project in IntelliJ IDEA

1. Open IntelliJ IDEA
2. Click **Open**
3. Select the `WebBasedApartmentSalesSystem` folder
4. Wait until the project indexing is completed
5. Allow IntelliJ to detect the Maven project

---

## 3. Reload Maven Dependencies

In IntelliJ IDEA:

1. Open the Maven panel
2. Click the reload icon

OR:

1. Right-click `pom.xml`
2. Select **Maven**
3. Click **Reload Project**

This downloads the required dependencies such as:

- SQL Server JDBC Driver
- Servlet API
- JSP API
- Jackson Databind
- JUnit

---

## 4. Create SQL Server Database

Open SQL Server Management Studio or Azure Data Studio.

Create a database named:

    Apartment_06

SQL command:

    CREATE DATABASE Apartment_06;
    GO

---

## 5. Run the Database Schema

Open this file:

    src/main/resources/schema.sql

Run the full script inside the `Apartment_06` database.

This will create all required tables, sequences, constraints, indexes, sample admin account, and sample FAQ records.

---

## 6. Configure Database Connection

Open:

    src/main/java/com/project/util/DBUtil.java

Find the database configuration section:

    private static final String URL = "jdbc:sqlserver://localhost:1433;databaseName=Apartment_06;encrypt=true;trustServerCertificate=true";
    private static final String USERNAME = "sa";
    private static final String PASSWORD = "12";

Update these values according to your local SQL Server setup.

Example:

    private static final String URL = "jdbc:sqlserver://localhost:1433;databaseName=Apartment_06;encrypt=true;trustServerCertificate=true";
    private static final String USERNAME = "sa";
    private static final String PASSWORD = "your_sql_server_password";

Make sure:

- SQL Server is running
- Port `1433` is enabled
- SQL Server Authentication is enabled
- The username and password are correct
- The database name is `Apartment_06`

---

## 7. Configure Tomcat Server in IntelliJ IDEA

1. Go to **Run**
2. Click **Edit Configurations**
3. Click **+**
4. Select **Tomcat Server**
5. Choose **Local**
6. Select your installed Tomcat directory
7. Go to the **Deployment** tab
8. Click **+**
9. Select **Artifact**
10. Choose the WAR exploded artifact for this project
11. Apply the configuration

Recommended application URL:

    http://localhost:8080/Apartment06/

If your Tomcat context path is different, use the URL shown by IntelliJ when the server starts.

---

## 8. Build the Project

You can build the project using IntelliJ Maven tools or terminal.

Terminal command:

    mvn clean package

This generates the WAR file inside the `target` folder.

---

## 9. Run the Application

Start the Tomcat configuration from IntelliJ IDEA.

After Tomcat starts successfully, open your browser and visit:

    http://localhost:8080/Apartment06/

If your context path is different, use the URL displayed in the Tomcat console.

---

## 🔐 Default Admin Login

The database schema inserts a default admin account.

| Field | Value |
|---|---|
| Username | admin |
| Email | admin@apartmentx.com |
| Password | admin123 |

Admin login page:

    http://localhost:8080/Apartment06/adminlogin.jsp

If login does not work, confirm that the `admins` table contains the default admin record after running `schema.sql`.

---

## 👤 User Flow

### Buyer Flow

1. Open the application
2. Register as a buyer
3. Login using buyer credentials
4. Browse apartments
5. View apartment details
6. Add apartments to favourites
7. Book an apartment
8. Add card details
9. Make payment
10. Submit review

---

### Seller Flow

1. Register as a seller
2. Login using seller credentials
3. Open seller dashboard
4. Add apartment listing
5. Edit apartment details
6. View listed apartments
7. Manage buyer bookings
8. View payment details

---

### Admin Flow

1. Open admin login page
2. Login using admin credentials
3. Access admin dashboard
4. Manage users
5. Manage apartments
6. Manage reviews
7. View reports
8. Update settings
9. Manage admin accounts

---

## 🌐 Important Pages

| Page | Purpose |
|---|---|
| index.jsp | Home page |
| login.jsp | Buyer/Seller login |
| register.jsp | Buyer/Seller registration |
| apartments.jsp | Apartment listing page |
| apartmentdetail.jsp | Apartment details |
| bookingform.jsp | Apartment booking form |
| buyerdashboard.jsp | Buyer dashboard |
| sellerdashboard.jsp | Seller dashboard |
| admindashboard.jsp | Admin dashboard |
| adminlogin.jsp | Admin login |
| buyerfavourites.jsp | Buyer favourites |
| buyerpayments.jsp | Buyer payment management |
| sellerpayments.jsp | Seller payment records |
| reviews.jsp | Review display |
| faq.jsp | Frequently asked questions |
| contact.jsp | Contact page |
| about.jsp | About page |

---

## 🔁 System Workflow

    User opens web application
        ↓
    JSP page displays interface
        ↓
    User submits form or clicks action
        ↓
    Servlet receives request
        ↓
    Service class processes business logic
        ↓
    DAO class communicates with SQL Server
        ↓
    Data is returned to Servlet
        ↓
    Servlet forwards or redirects to JSP
        ↓
    User sees updated result

---

## 🧪 Testing the Database Connection

If the application does not connect to the database:

1. Confirm SQL Server is running
2. Confirm database name is `Apartment_06`
3. Confirm username and password in `DBUtil.java`
4. Confirm SQL Server port `1433` is enabled
5. Confirm SQL Server JDBC dependency is loaded by Maven
6. Reload Maven
7. Restart Tomcat

---

## ⚠️ Common Issues and Fixes

### Maven dependencies are not loading

Reload Maven:

    Right-click pom.xml → Maven → Reload Project

Or run:

    mvn clean install

---

### Tomcat server not starting

Check:

- Tomcat is installed correctly
- Correct Tomcat version is selected
- Port `8080` is not already in use
- WAR artifact is deployed properly

If port `8080` is already used, change the Tomcat port in server configuration.

---

### Database connection failed

Check `DBUtil.java`:

    private static final String URL = "jdbc:sqlserver://localhost:1433;databaseName=Apartment_06;encrypt=true;trustServerCertificate=true";
    private static final String USERNAME = "sa";
    private static final String PASSWORD = "your_password";

Also check:

- SQL Server Authentication is enabled
- SQL Server service is running
- TCP/IP is enabled in SQL Server Configuration Manager
- Port 1433 is active
- Database exists

---

### Login not working

Check:

- Database tables were created correctly
- User exists in the `users` table
- Admin exists in the `admins` table
- Password matches the stored value
- The application is connected to the correct database

---

### JSP page not found

Check:

- Tomcat deployment artifact is added
- Context path is correct
- URL includes the application context path

Example:

    http://localhost:8080/Apartment06/

---

### SQL script error

Make sure you are running the script on Microsoft SQL Server, not MySQL.

This project uses SQL Server syntax such as:

- `NVARCHAR`
- `DATETIME2`
- `GO`
- `SEQUENCE`
- `SYSUTCDATETIME()`

---

## 📦 Maven Dependencies

Main dependencies used in this project:

| Dependency | Purpose |
|---|---|
| mssql-jdbc | Connect Java application with SQL Server |
| javax.servlet-api | Servlet support |
| javax.servlet.jsp-api | JSP support |
| jackson-databind | JSON/data binding support |
| junit | Testing support |

---

## 🔐 Security Note

The current database credentials are stored directly inside `DBUtil.java`.

For production usage, it is recommended to move database credentials to:

- Environment variables
- External configuration file
- Server-level secrets
- Secure deployment configuration

Also avoid using simple passwords in real deployments.

---

## 🔮 Future Improvements

Possible improvements for this project:

- Add password hashing for all users and admins
- Move database credentials to environment variables
- Add role-based access filters
- Improve form validation
- Add apartment image upload storage improvements
- Add email notifications for bookings
- Add payment gateway integration
- Add advanced apartment search filters
- Add dashboard charts and analytics
- Add REST API support
- Add unit and integration tests
- Add deployment guide for cloud hosting
- Improve mobile responsiveness
- Add forgot password feature
- Add seller verification workflow

---

## 👨‍💻 Author

**Himaka Uthpala**

GitHub: https://github.com/Himaka12

---

## 📄 License

This project currently does not include a license file.

You can add an open-source license such as the MIT License if you want others to use, modify, and contribute to this project.

---

## ⭐ Support

If you found this project useful, consider giving the repository a star on GitHub.

---

## ✅ Final Note

The **Web Based Apartment Sales System** is a complete Java web application built with JSP, Servlets, Maven, Apache Tomcat, and Microsoft SQL Server. It includes buyer, seller, and admin workflows with apartment management, booking management, payment handling, review management, favourites, profile management, and FAQ support.


