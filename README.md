# Airbnb Clone Project

## Overview
The **Airbnb Clone Project** is a full-stack web application inspired by Airbnb, built as part of the ALX Backend Prodev Cohort.  
The goal is to recreate the core functionality of Airbnb — allowing users to list, discover, and book properties — while focusing on clean architecture, scalability, and maintainable backend design.

This backend forms the foundation of the entire system, handling user authentication, property management, bookings, payments, and reviews through well-structured APIs.

---

## Project Goals
- **User Management:** Secure registration, authentication, and profile management.  
- **Property Management:** Create, update, and manage property listings.  
- **Booking System:** Enable users to make and manage property reservations.  
- **Payment Processing:** Integrate a system for handling and tracking transactions.  
- **Review System:** Allow users to share feedback and ratings.  
- **Performance:** Optimize data retrieval and storage for efficiency and speed.

---

## Technology Stack
**Backend:** Django, Django REST Framework  
A Python web framework used to build the backend and RESTful APIs. 
Provides tools to create and manage RESTful APIs efficiently.  
**Database:** PostgreSQL  
A relational database for storing users, properties, bookings, and reviews.  
**API Design:** REST + GraphQL  
Offers flexible and efficient querying of backend data. 
**Task Management:** Celery, Redis  
Handles asynchronous tasks like notifications and payment processing. 
Used for caching and session management to improve performance.   
**Containerization:** Docker  
Containerizes the application for consistent development and deployment. 
**CI/CD:** Automated testing and deployment pipelines

---

## Feature Breakdown

### **User Management**
Handles registration, authentication, and profile management for both guests and hosts.  
This feature ensures that users can securely sign up, log in, and manage their personal information, providing a foundation for personalized interactions and bookings.

### **Property Management**
Allows hosts to create, update, and manage property listings.  
Users can view property details, photos, pricing, and availability, making it easy to browse and select accommodations.

### **Booking System**
Enables guests to reserve properties and manage their reservations.  
It handles check-in/check-out dates, booking status, and availability, ensuring a smooth and reliable reservation process.

### **Payment Processing**
Facilitates secure transactions for bookings.  
This feature records payment details, tracks payment status, and integrates with payment gateways to process guest payments safely.

### **Review System**
Allows guests to leave feedback and ratings for properties they stayed at.  
Reviews help future guests make informed decisions and provide hosts with valuable insights to improve their offerings.

### **API Documentation**
Provides clear documentation of all available endpoints using OpenAPI standards and GraphQL queries.  
It helps developers and integrators understand how to interact with the backend efficiently.

---

## Database Design

The Airbnb Clone backend uses a relational database (PostgreSQL) to manage users, properties, bookings, reviews, and payments. Below is an overview of the main entities and their relationships.

### **Users**
Key fields: `id`, `name`, `email`, `password`, `role`  
- Represents individuals using the platform as guests or hosts.  
- A user can have multiple properties (if they are a host) and multiple bookings (if they are a guest).

### **Properties**
Key fields: `id`, `host_id`, `title`, `description`, `price`, `location`  
- Represents listings available for booking.  
- Each property belongs to a single host (user) and can have multiple bookings and reviews.

### **Bookings**
Key fields: `id`, `user_id`, `property_id`, `check_in`, `check_out`, `status`  
- Represents a reservation made by a user for a property.  
- Each booking belongs to one user (guest) and one property.

### **Reviews**
Key fields: `id`, `user_id`, `property_id`, `rating`, `comment`, `created_at`  
- Represents feedback left by users for properties they stayed at.  
- Each review is associated with one user and one property.

### **Payments**
Key fields: `id`, `booking_id`, `amount`, `payment_method`, `status`, `created_at`  
- Represents transactions made by users for bookings.  
- Each payment is linked to a single booking and, indirectly, to a user and property.

---

### **Entity Relationships**
- **User ↔ Property:** One-to-Many (a user can host multiple properties)  
- **User ↔ Booking:** One-to-Many (a user can make multiple bookings)  
- **Property ↔ Booking:** One-to-Many (a property can have multiple bookings)  
- **Property ↔ Review:** One-to-Many (a property can have multiple reviews)  
- **Booking ↔ Payment:** One-to-One (each booking has one payment record)

---

## API Overview
| Module | Endpoints | Description |
|---------|------------|-------------|
| **Users** | `/users/`, `/users/{id}/` | Manage user registration and profiles |
| **Properties** | `/properties/`, `/properties/{id}/` | Create and manage property listings |
| **Bookings** | `/bookings/`, `/bookings/{id}/` | Handle reservations and booking details |
| **Payments** | `/payments/` | Process and record transactions |
| **Reviews** | `/reviews/`, `/reviews/{id}/` | Manage property feedback and ratings |

---

## Team Roles
This project is developed collaboratively as part of the **ALX Backend Prodev Cohort**, involving:
- **Backend Developers:** API endpoints and business logic.
Implements the application’s logic, APIs, and database interactions.  
In this project, backend developers handle core modules such as authentication, property management, bookings, payments, and reviews, ensuring everything runs efficiently and securely.  
- **Database Admins:** Schema design and query optimization.  
Designs, manages, and optimizes the database layer.  
They ensure data consistency, performance, and reliability—especially as the application scales and handles more users and listings.
- **DevOps Engineers:** Deployment, monitoring, and scaling. 
Bridges development and operations to streamline the release process.  
They set up and maintain CI/CD pipelines, monitor deployments, and automate workflows so that updates reach production quickly and safely. 
- **QA Engineers:** Testing for performance, reliability, and usability.
Tests the application to make sure it works as expected.  
They check both functionality and performance, identify bugs early, and confirm that every release meets quality standards.

---

## Summary
This project aims to replicate the Airbnb experience through modern backend practices — combining Django’s reliability, REST and GraphQL flexibility, and containerized deployment.  
It’s not just about cloning Airbnb, but about mastering real-world backend architecture, scalability, and clean API design.

---

**Author:** Soala George  
**Cohort:** ALX Backend Prodev