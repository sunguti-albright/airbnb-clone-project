# AIRBNB CLONE PROJECT 🏡

## Developer

[Ms. Albright Sunguti](https://albright-portfolio.vercel.app/)

## About the project  :woman_technologist:
The Goal of this project is to develop a comprehensive, real-world application designed to simulate the development of a robust booking platform like Airbnb. It involves a deep dive into full-stack development, focusing on backend systems, database design, API development, and application security.

# AirBNB Clone Frontend Documentation

## Tech Stack Used
+ Frontend: React (HTML, CSS, JavaScript)

+ Backend: Python (Django)

+ Version Control: Git & GitHub

+ Design Tools: Figma``

+ Hosting: AWS

## UI/UX Design Planning

### Design Goals
- Create an intuitive and seamless booking flow  
- Maintain visual consistency across pages  
- Ensure fast loading and responsiveness  
- Prioritize mobile-first design  
- Meet accessibility standards (WCAG guidelines)  

### Key Features
- Property search and filtering  
- Detailed property viewing (images, amenities, reviews, availability)  
- Secure and simple checkout process  
- User authentication for bookings and profiles  

### Primary Pages

| Page | Description |
|------|-------------|
| **Property Listing View** | Displays a grid of available properties with filters (location, price, amenities, rating). |
| **Listing Detailed View** | Shows full property details: images, host info, amenities, reviews, map, and booking form. |
| **Simple Checkout View** | Streamlined page for entering guest details, reviewing booking summary, and confirming payment. |

### Importance of a User-Friendly Design
A user-friendly booking system minimizes friction, increases trust, and encourages conversions. Clear navigation, responsive layouts, and transparent pricing help users make confident decisions, while accessibility ensures the platform is usable by a wider audience.

## Figma Design Specifications 
The figma design can be accessed [here](https://www.figma.com/design/E2BRqdPcKkrnX6hLGPto8Z/Project-Airbnb?node-id=1-4)

**Color Styles**  
- Primary: `#FF5A5F`  
- Secondary: `#008489`  
- Background: `#FFFFFF`  
- Text: `#222222`  
- Secondary Text: `#717171`  

**Typography**  
- Primary Font: Circular  
- Headings: Font weight Bold (700), font size 24px–32px  
- Body Text: Medium (500), 16px  
- Secondary Text: Book (400), 14px 

**Why Identifying Design Properties Matters**  
Defining design properties like color and typography ensures visual consistency, brand identity, and scalability. It helps both designers and developers work faster by providing a shared visual guide for building the interface.

## Project Roles and Responsibilities

+ Project Manager -	Oversees timeline, coordinates team, manages deliverables
+ Frontend Developers - Implements UI components, ensures responsive design
+ Backend Developers	- Builds APIs, manages database, implements business logic
+ Designers	- Creates mockups, maintains design system, ensures UX quality
+ QA/Testers	- Writes test cases, performs testing, reports bugs
+ DevOps Engineers	- Manages deployment, CI/CD pipeline, server infrastructure
+ Product Owner	- Defines requirements, prioritizes features, represents stakeholders
+ Scrum Master	- Facilitates agile processes, removes blockers, organizes meetings

## UI Component Patterns ✨

### Planned Components

**Navbar**  
- Logo  
- Search bar  
- User navigation (login/profile)  
- Responsive menu for mobile  

**Property Card**  
- Property image  
- Basic details (price, location, rating)  
- Favorite button (wishlist)  
- Responsive layout for grid display  

**Footer**  
- Site links (About, Contact, Help)  
- Company information  
- Social media links  
- Copyright  

### Why Component Patterns Matter
Planning UI components ensures **reusability, consistency, and scalability**. It helps maintain a unified look and feel across the app, reduces development time, and allows for easier updates as the project grows.

# AirBNB Clone Backend Documentation

## 🚀 Objective
The backend for the Airbnb Clone project is designed to provide a robust and scalable foundation for managing user interactions, property listings, bookings, and payments. This backend will support various functionalities required to mimic the core features of Airbnb, ensuring a smooth experience for users and hosts.

## Project Goals
---

## 🏆 Project Goals
- **User Management:** Implement a secure system for user registration, authentication, and profile management.  
- **Property Management:** Develop features for property listing creation, updates, and retrieval.  
- **Booking System:** Create a booking mechanism for users to reserve properties and manage booking details.  
- **Payment Processing:** Integrate a payment system to handle transactions and record payment details.  
- **Review System:** Allow users to leave reviews and ratings for properties.  
- **Data Optimization:** Ensure efficient data retrieval and storage through database optimizations.  

---

## 👥 Team Roles
- **Backend Developer:** Implements API endpoints, database schemas, and business logic.  
- **Database Administrator:** Manages database design, indexing, and optimizations.  
- **DevOps Engineer:** Handles deployment, monitoring, and scaling of backend services.  
- **QA Engineer:** Ensures the backend functionalities are thoroughly tested and meet quality standards.  

---


## ⚙️ Technology Stack
- **Django** – A high-level Python web framework used for building the RESTful API.  
- **Django REST Framework** – Provides tools for creating and managing RESTful APIs.  
- **PostgreSQL** – A powerful relational database used for data storage.  
- **GraphQL** – Allows for flexible and efficient querying of data.  
- **Celery** – For handling asynchronous tasks such as sending notifications or processing payments.  
- **Redis** – Used for caching and session management.  
- **Docker** – Containerization tool for consistent development and deployment environments.  
- **CI/CD Pipelines** – Automated pipelines for testing and deploying code changes.  

---

## 🗄️ Database Design

### Entities & Fields
- **Users**
  - id (PK)  
  - username  
  - email  
  - password_hash  
  - created_at  

- **Properties**
  - id (PK)  
  - user_id (FK → Users)  
  - title  
  - description  
  - price_per_night  
  - location  

- **Bookings**
  - id (PK)  
  - property_id (FK → Properties)  
  - user_id (FK → Users)  
  - start_date  
  - end_date  
  - status  

- **Reviews**
  - id (PK)  
  - property_id (FK → Properties)  
  - user_id (FK → Users)  
  - rating  
  - comment  

- **Payments**
  - id (PK)  
  - booking_id (FK → Bookings)  
  - amount  
  - status  
  - payment_date  

### Relationships
- A **User** can have multiple **Properties**.  
- A **Booking** belongs to one **Property** and one **User**.  
- A **Payment** is tied to a single **Booking**.  
- A **Review** is linked to both a **Property** and a **User**.  

---

## 🔑 Feature Breakdown
- **User Management:** Provides authentication, registration, and profile management to ensure secure access.  
- **Property Management:** Allows hosts to create, update, and manage property listings.  
- **Booking System:** Enables users to book properties, check availability, and manage reservations.  
- **Payment Processing:** Ensures secure handling of financial transactions.  
- **Review System:** Builds trust by letting users leave feedback on properties.  
- **Database Optimization:** Improves system performance through indexing and caching.  

---
## 🛠️ Features Overview

### 1. API Documentation
- **Django REST Framework:** Provides a comprehensive RESTful API for handling CRUD operations on user and property data.  
- **GraphQL:** Offers a flexible and efficient query mechanism for interacting with the backend.  

### 2. User Authentication
- **Endpoints:** `/users/`, `/users/{user_id}/`  
- **Features:** Register new users, authenticate, and manage user profiles.  

### 3. Property Management
- **Endpoints:** `/properties/`, `/properties/{property_id}/`  
- **Features:** Create, update, retrieve, and delete property listings.  

### 4. Booking System
- **Endpoints:** `/bookings/`, `/bookings/{booking_id}/`  
- **Features:** Make, update, and manage bookings, including check-in and check-out details.  

### 5. Payment Processing
- **Endpoints:** `/payments/`  
- **Features:** Handle payment transactions related to bookings.  

### 6. Review System
- **Endpoints:** `/reviews/`, `/reviews/{review_id}/`  
- **Features:** Post and manage reviews for properties.  

### 7. Database Optimizations
- **Indexing:** Implement indexes for fast retrieval of frequently accessed data.  
- **Caching:** Use caching strategies to reduce database load and improve performance.  

---

## 📈 API Documentation Overview
- **REST API:** Detailed documentation available through the OpenAPI standard, including endpoints for users, properties, bookings, and payments.  
- **GraphQL API:** Provides a flexible query language for retrieving and manipulating data.  

---

## 📌 Endpoints Used
### Users
- `GET /users/` – List all users  
- `POST /users/` – Create a new user  
- `GET /users/{user_id}/` – Retrieve a specific user  
- `PUT /users/{user_id}/` – Update a specific user  
- `DELETE /users/{user_id}/` – Delete a specific user  

### Properties
- `GET /properties/` – List all properties  
- `POST /properties/` – Create a new property  
- `GET /properties/{property_id}/` – Retrieve a specific property  
- `PUT /properties/{property_id}/` – Update a specific property  
- `DELETE /properties/{property_id}/` – Delete a specific property  

### Bookings
- `GET /bookings/` – List all bookings  
- `POST /bookings/` – Create a new booking  
- `GET /bookings/{booking_id}/` – Retrieve a specific booking  
- `PUT /bookings/{booking_id}/` – Update a specific booking  
- `DELETE /bookings/{booking_id}/` – Delete a specific booking  

### Payments
- `POST /payments/` – Process a payment  

### Reviews
- `GET /reviews/` – List all reviews  
- `POST /reviews/` – Create a new review  
- `GET /reviews/{review_id}/` – Retrieve a specific review  
- `PUT /reviews/{review_id}/` – Update a specific review  
- `DELETE /reviews/{review_id}/` – Delete a specific review  

---

## 🔐 API Security
- **Authentication:** JWT-based authentication for secure access.  
- **Authorization:** Role-based access control (e.g., host vs. guest).  
- **Rate Limiting:** Prevents abuse by limiting API calls.  
- **Data Protection:** Encrypt sensitive data (passwords, payments).  

🔒 Security is critical to:  
- Protect user data (personal info, credentials).  
- Ensure financial transactions are safe.  
- Prevent unauthorized access to property/booking data.  

---

## ⚡ CI/CD Pipeline
- **What is CI/CD?**  
  Continuous Integration/Continuous Deployment automates testing and deployment to maintain code quality and speed up releases.  

- **Tools:**  
  - GitHub Actions for automated builds/tests.  
  - Docker for consistent containerized environments.  
  - Deployment to cloud services (AWS).  

---

📌 **Repo:** [airbnb-clone-project](https://github.com/your-username/airbnb-clone-project)  
📄 **Developed with enthusiasm and lots (I mean Lots 👩🏽) of Coffee ☕**
