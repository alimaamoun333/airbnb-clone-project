# Airbnb Clone Project

## Overview
The Airbnb Clone Project is a full-stack web application that replicates the core functionality of Airbnb. It helps users list properties, book stays, and manage their experiences securely.

## Project Goals
- Learn collaborative development using GitHub.
- Implement backend logic using Django.
- Practice database design and integration with PostgreSQL.
- Learn CI/CD practices for smooth deployment.


## Team Roles

### Backend Developer
Responsible for building APIs, handling authentication, and managing business logic using Django.

### Database Administrator (DBA)
Designs, manages, and optimizes the PostgreSQL database. Ensures data integrity and relationships.

### DevOps Engineer
Implements CI/CD pipelines using tools like GitHub Actions and Docker. Manages containerization and deployment.

### Project Manager
Coordinates task assignments, monitors deadlines, and ensures smooth team collaboration.

### Frontend Developer (optional)
If added to the team, works on building the UI components and integrates them with APIs.


## Technology Stack

### Django
A Python web framework for building secure and scalable APIs and web apps.

### PostgreSQL
A relational database used to store and manage user, booking, and property data.

### GraphQL
A flexible query language for APIs, allowing clients to request only the data they need.

### Docker
Used to containerize the app and services for consistent development and deployment.

### GitHub Actions
A CI/CD tool that automates testing and deployment every time you push code.


## Database Design

### Entities and Fields

**Users**
- id
- name
- email
- password (hashed)
- created_at

**Properties**
- id
- user_id (FK)
- title
- location
- price_per_night
- created_at

**Bookings**
- id
- user_id (FK)
- property_id (FK)
- start_date
- end_date

**Reviews**
- id
- user_id (FK)
- property_id (FK)
- rating
- comment

**Payments**
- id
- booking_id (FK)
- amount
- payment_method
- status

### Relationships
- A user can list multiple properties.
- A user can make multiple bookings.
- Each booking is linked to one user and one property.
- A property can have many reviews.
- Each payment is linked to a specific booking.


## Feature Breakdown

### User Management
Allows users to register, log in, and manage their profiles. Ensures secure access to features.

### Property Management
Hosts can list properties with descriptions, images, prices, and availability.

### Booking System
Enables users to book available properties for specific dates and view booking history.

### Review System
After completing a stay, users can leave ratings and comments for properties.

### Payment Integration
Handles secure payment processing for bookings using external APIs or mock gateways.


## API Security

### Authentication
Only registered users can access protected endpoints using JWT or token-based authentication.

### Authorization
Users can only access or modify their own data (e.g., cannot delete others’ bookings).

### Rate Limiting
Limits the number of requests to the API to prevent abuse or DDoS attacks.

### Data Validation & Encryption
Validates inputs and securely stores sensitive data (e.g., hashed passwords, encrypted payments).

### Why Security Matters
- Protects user data from breaches.
- Prevents unauthorized access.
- Secures financial transactions.


## CI/CD Pipeline

CI/CD (Continuous Integration and Continuous Deployment) automates testing, building, and deploying the application.

### Why It’s Important
- Ensures code is tested before going live.
- Speeds up the deployment process.
- Reduces human error in production deployments.

### Tools Used
- **GitHub Actions**: For running tests and builds on each push.
- **Docker**: For creating consistent development and production environments.


