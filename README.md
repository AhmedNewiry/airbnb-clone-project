# Airbnb Clone Project

## Overview
The Airbnb Clone Project is a full-stack web application designed to replicate core functionalities of a booking platform like Airbnb. The goal is to create a scalable, secure, and user-friendly platform that allows users to list, discover, and book accommodations. This project leverages modern backend frameworks, database systems, and CI/CD pipelines to simulate real-world software development practices, focusing on collaborative workflows, API security, and robust database design.

## Team Roles
- **Backend Developer**: Responsible for building and maintaining the server-side logic, APIs, and integrations with the database. They ensure the application is scalable, secure, and performs efficiently under varying loads.
- **Database Administrator**: Designs and manages the database schema, optimizes queries, and ensures data integrity and security. They handle backups, migrations, and performance tuning for the database system.
- **DevOps Engineer**: Sets up and maintains CI/CD pipelines, containerization (e.g., Docker), and deployment workflows. They focus on automating processes to improve development efficiency and reduce errors.
- **QA Engineer**: Tests the application to identify bugs, ensure functionality meets requirements, and validate user experience. They create test cases and collaborate with developers to resolve issues.

## Technology Stack
- **Django**: A Python-based web framework used for building RESTful APIs and handling server-side logic, enabling rapid development and secure application structure.
- **PostgreSQL**: A relational database management system used for storing and managing data, offering robust support for complex queries and scalability.
- **GraphQL**: A query language for APIs that allows clients to request specific data, improving efficiency and flexibility in data retrieval.
- **Docker**: A containerization platform used to package the application and its dependencies, ensuring consistent environments across development, testing, and production.

## Database Design
- **Users**: Fields: `user_id` (primary key), `email`, `password_hash`, `name`, `phone`. Relationships: A user can own multiple properties and create multiple bookings or reviews.
- **Properties**: Fields: `property_id` (primary key), `owner_id` (foreign key to Users), `title`, `description`, `price_per_night`. Relationships: A property belongs to one user and can have multiple bookings and reviews.
- **Bookings**: Fields: `booking_id` (primary key), `property_id` (foreign key to Properties), `user_id` (foreign key to Users), `start_date`, `end_date`. Relationships: A booking is associated with one property and one user.
- **Reviews**: Fields: `review_id` (primary key), `property_id` (foreign key to Properties), `user_id` (foreign key to Users), `rating`, `comment`. Relationships: A review is linked to one property and one user.
- **Payments**: Fields: `payment_id` (primary key), `booking_id` (foreign key to Bookings), `amount`, `payment_date`, `status`. Relationships: A payment is tied to one booking.