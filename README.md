# AirBnB Clone Project

## Overview
This project is a simplified clone of the AirBnB web application, designed to demonstrate and practice full-stack web development skills. It mimics features like user registration, property listings, and booking.

## Project Goals
- Learn full-stack web development
- Build backend and frontend components from scratch
- Practice version control with Git and GitHub
- Collaborate on a team-based software project

## Tech Stack
- **Backend**: Python, Django
- **Frontend**: HTML, CSS, JavaScript
- **Database**: MySQL or SQLite
- **Tools**: Git, GitHub, Postman, Ubuntu/Linux CLI

## Author
Yvonne Bosibori
## Team Roles

### Backend Developer
Responsible for building the core functionality of the application, such as handling server-side logic, APIs, authentication, and integrating with the database using frameworks like Django.

### Frontend Developer
Focuses on the user interface and user experience by building responsive layouts using HTML, CSS, and JavaScript. Ensures users can interact smoothly with the application.

### Database Administrator (DBA)
Designs, implements, and manages the database systems. Ensures data is structured correctly, runs efficiently, and is securely backed up.

### DevOps Engineer
Manages deployment, CI/CD pipelines, and cloud infrastructure. Ensures the application is reliably hosted, monitored, and updated.

### UI/UX Designer
Creates the layout, color scheme, and user flow of the application. Makes sure the app is both visually appealing and user-friendly.

### Project Manager
Coordinates the team, manages timelines, tracks progress, and ensures that project goals are met on time and within scope.

### Quality Assurance (QA) Tester
Tests the application for bugs, usability issues, and performance problems. Makes sure the product meets all requirements before going live.
## Technology Stack

### Django
A high-level Python web framework used to build the backend of the application. It enables fast development and clean design, ideal for building RESTful APIs and handling business logic.

### PostgreSQL
A powerful open-source relational database system used to store and manage user data, listings, bookings, and more. It works seamlessly with Django for efficient data operations.

### HTML/CSS
Used to build and style the frontend pages that users interact with. HTML structures the content, while CSS makes it visually appealing.

### JavaScript
Adds interactivity to the frontend, such as form validation, dynamic page updates, and user interface enhancements.

### Git & GitHub
Used for version control and collaboration. Tracks code changes and allows multiple developers to work on the project simultaneously.

### Postman
A tool for testing and documenting RESTful APIs. Helps ensure that API endpoints function correctly and return the expected data.

### Ubuntu/Linux Terminal
The command line interface used for running scripts, managing the server, setting permissions, and deploying the application.

### Virtual Environments (venv)
Isolates Python packages for the project to prevent conflicts with system-wide packages and dependencies.

## Database Design
###  Users
**Fields:**
- `id` (Primary Key)
- `name`
- `email`
- `password_hash`
- `created_at`

**Relationships:**
- A user can list multiple properties
- A user can make multiple bookings
- A user can leave multiple reviews

---

###  Properties
**Fields:**
- `id` (Primary Key)
- `title`
- `description`
- `location`
- `price_per_night`
- `owner_id` (Foreign Key to Users)

**Relationships:**
- A property belongs to one user (the owner)
- A property can have multiple bookings and reviews

---

### Bookings
**Fields:**
- `id` (Primary Key)
- `user_id` (Foreign Key to Users)
- `property_id` (Foreign Key to Properties)
- `start_date`
- `end_date`
- `total_price`

**Relationships:**
- A booking belongs to one user
- A booking is linked to one property

---

### Reviews
**Fields:**
- `id` (Primary Key)
- `user_id` (Foreign Key to Users)
- `property_id` (Foreign Key to Properties)
- `rating` (1–5)
- `comment`

**Relationships:**
- A review is written by a user for a property
- A property can have many reviews

---

###  Payments
**Fields:**
- `id` (Primary Key)
- `booking_id` (Foreign Key to Bookings)
- `amount`
- `payment_method`
- `payment_status`

**Relationships:**
- A payment is linked to a specific booking

## Feature Breakdown
###  User Management
Allows users to register, log in, and manage their profiles securely. This feature handles authentication and ensures that only authorized users can access or modify data.

###  Property Management
Enables hosts to list their properties with details such as title, description, location, and pricing. It provides a platform for managing multiple listings and updating information as needed.

###  Booking System
Users can search for properties, select available dates, and make reservations. This system ensures availability tracking and prevents booking conflicts.

###  Payment Processing
Integrates payment functionality so users can securely pay for bookings. It includes payment confirmation and error handling for failed transactions.

###  Review & Rating System
Users can leave reviews and rate properties after their stay. This builds trust and helps future guests make informed decisions.

###  Search and Filters
Allows users to search for properties based on location, price range, dates, and other filters. This enhances user experience by quickly narrowing down relevant options.

### Admin Dashboard (optional)
An admin interface to manage users, properties, bookings, and reviews. It provides oversight and control over the platform’s operations.

## API Security

Securing the backend APIs is essential to protect sensitive user data, ensure application integrity, and maintain user trust. The following key security measures will be implemented in this project:

### Authentication
Only registered and verified users will be allowed to access protected endpoints. Authentication mechanisms such as token-based authentication (e.g., JWT) will be used to ensure users are who they claim to be.

### ️ Authorization
Controls will be in place to ensure users can only perform actions they’re permitted to. For example, only property owners can edit or delete their listings, while general users can only view and book properties.

###  Rate Limiting
To prevent abuse or brute-force attacks, rate limiting will be implemented to restrict the number of API requests a user can make within a certain time frame.

###  Data Protection
Sensitive information like passwords will be hashed, and personal user data will be securely stored and transferred using HTTPS.

###  Securing Payments
Payment processes will be handled using secure gateways, ensuring that financial transactions are encrypted and protected against fraud or interception.

Implementing these measures ensures that the platform is safe, reliable, and trustworthy for all users.
