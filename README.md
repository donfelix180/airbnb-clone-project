# airbnb-clone-project

## Project Overview
This project is a full-stack web application that replicates the core functionalities of the popular booking platform, Airbnb. The goal is to build a robust and scalable platform for listing properties and making reservations.

## Technology Stack
This project will utilize a modern tech stack to ensure high performance and maintainability. Key technologies include Django for the backend, PostgreSQL as the database, and potentially GraphQL for the API layer.

## Team Roles
This section outlines the key roles and responsibilities within the project team.

### Backend Developer
*   **Responsibility:** Develops and maintains the server-side logic, API endpoints, and database interactions.
*   **Contribution:** Writes the code for user authentication, property management, and the booking system.

### Database Administrator
*   **Responsibility:** Designs, implements, and manages the project's database system.
*   **Contribution:** Defines database schemas, ensures data integrity, and optimizes database performance.

### Frontend Developer
*   **Responsibility:** Creates the user-facing interface and user experience.
*   **Contribution:** Develops the web pages for displaying properties, handling user input, and managing bookings.

### DevOps Engineer
*   **Responsibility:** Manages the CI/CD pipeline, deployment process, and infrastructure.
*   **Contribution:** Automates the build, test, and deployment phases to ensure continuous and reliable delivery.

## Technology Stack
This project will utilize a modern and efficient technology stack.

*   **Django:** A high-level Python web framework used for building the application's backend and creating a robust, RESTful API.
*   **PostgreSQL:** A powerful, open-source object-relational database system used for storing the project's data, including users, properties, and bookings.
*   **GraphQL:** An API query language that allows for more efficient data fetching from the backend.
*   **React:** A JavaScript library for building the user interface, enabling the creation of dynamic and single-page application features.
## Database Design
The database is structured around key entities that manage user information, property listings, and reservations.

### Entities
*   **Users:** Stores information about users registered on the platform.
    *   `id` (Primary Key)
    *   `username`
    *   `email`
    *   `password_hash`
    *   `is_host` (boolean)
*   **Properties:** Contains details of properties available for booking.
    *   `id` (Primary Key)
    *   `host_id` (Foreign Key to Users)
    *   `title`
    *   `description`
    *   `price_per_night`
*   **Bookings:** Stores reservation details made by users.
    *   `id` (Primary Key)
    *   `user_id` (Foreign Key to Users)
    *   `property_id` (Foreign Key to Properties)
    *   `check_in_date`
    *   `check_out_date`
*   **Reviews:** Stores reviews submitted by users for properties.
    *   `id` (Primary Key)
    *   `user_id` (Foreign Key to Users)
    *   `property_id` (Foreign Key to Properties)
    *   `rating`
    *   `comment`
*   **Payments:** Manages payment records related to bookings.
    *   `id` (Primary Key)
    *   `booking_id` (Foreign Key to Bookings)
    *   `amount`
    *   `status`
    *   `transaction_id`

### Entity Relationships
*   A **User** can have multiple **Properties** (if they are a host).
*   A **User** can create multiple **Bookings**.
*   A **Booking** belongs to one **User** and one **Property**.
*   A **User** can write multiple **Reviews**, and a **Property** can have multiple **Reviews**.
*   A **Booking** can have one **Payment**.

