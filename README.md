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

## Tech Stack
**Backend:** Django, Django REST Framework  
**Database:** PostgreSQL  
**API Design:** REST + GraphQL  
**Task Management:** Celery, Redis  
**Containerization:** Docker  
**CI/CD:** Automated testing and deployment pipelines

---

## Features
- **Comprehensive API:** Built with Django REST Framework and documented using OpenAPI.  
- **Flexible Queries:** GraphQL layer for efficient and customizable data retrieval.  
- **Caching & Optimization:** Redis and database indexing for better performance.  
- **Asynchronous Processing:** Celery handles background tasks like notifications and payments.  
- **Secure Authentication:** Token-based user access and session management.

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

## Roles & Collaboration
This project is developed collaboratively as part of the **ALX Backend Prodev Cohort**, involving:
- **Backend Developers:** API endpoints and business logic.  
- **Database Admins:** Schema design and query optimization.  
- **DevOps Engineers:** Deployment, monitoring, and scaling.  
- **QA Engineers:** Testing for performance, reliability, and usability.

---

## Summary
This project aims to replicate the Airbnb experience through modern backend practices — combining Django’s reliability, REST and GraphQL flexibility, and containerized deployment.  
It’s not just about cloning Airbnb, but about mastering real-world backend architecture, scalability, and clean API design.

---

**Author:** Soala George  
**Cohort:** ALX Backend Prodev