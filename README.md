# Airbnb Clone Project

## Overview

This project is a full-stack clone of the Airbnb platform.

## Project Goals

- Understand and implement a modern web application architecture.

- Practice full-stack development with real-world features.

- Gain experience using technologies commonly used in production environments.

## Tech Stack

- **Frontend:**

- **Backend:**

- **Database:**

- **Authentication:**

- **Deployment:**

## Team Roles

Below are the key roles involved in the development of the Airbnb Clone Project, along with their responsibilities:

### 👨‍💻 Backend Developer

Responsible for building the server-side logic, APIs, and integrating the frontend with the database. Ensures secure, scalable, and efficient handling of requests.

### 🎨 Frontend Developer

Handles the client-side of the application using React. Focuses on building user interfaces, ensuring responsiveness, and delivering a smooth user experience.

### 🛢️ Database Administrator (DBA)

Designs and manages the database schema, ensures data integrity and performance optimization, and handles backups and migrations.

### 🔐 DevOps Engineer

Automates deployment, monitors infrastructure, and ensures continuous integration/continuous deployment (CI/CD). Handles cloud configurations and system reliability.

### 📐 UI/UX Designer

Designs the application's layout and user flow. Ensures the platform is intuitive, accessible, and visually appealing to end-users.

### 🧪 QA Engineer

Develops and executes test plans to identify bugs and ensure that new features do not break existing functionality. Maintains the quality and reliability of the application.

### 📋 Project Manager

Coordinates the team's efforts, tracks progress, sets deadlines, and ensures the project meets business goals. Acts as a liaison between developers and stakeholders.

## Database Design

This section outlines the core entities in our Airbnb Clone application, along with their key fields and relationships.

### 🧑 Users

Represents individuals using the platform, either as guests or hosts.

**Key Fields:**

- `id` (Primary Key)
- `name`
- `email`
- `password_hash`
- `is_host` (boolean)

**Relationships:**

- A user can list multiple properties (1:N).
- A user can make multiple bookings (1:N).
- A user can leave multiple reviews (1:N).

---

### 🏠 Properties

Represents the listings created by hosts.

**Key Fields:**

- `id` (Primary Key)
- `user_id` (Foreign Key to Users)
- `title`
- `description`
- `location`
- `price_per_night`

**Relationships:**

- A property belongs to a user (N:1).
- A property can have many bookings (1:N).
- A property can have many reviews (1:N).

---

### 📅 Bookings

Represents reservations made by guests for properties.

**Key Fields:**

- `id` (Primary Key)
- `user_id` (Foreign Key to Users)
- `property_id` (Foreign Key to Properties)
- `start_date`
- `end_date`
- `total_price`

**Relationships:**

- A booking belongs to a user and a property (N:1).
- A booking can have one payment (1:1).

---

### ⭐ Reviews

Represents user feedback on properties.

**Key Fields:**

- `id` (Primary Key)
- `user_id` (Foreign Key to Users)
- `property_id` (Foreign Key to Properties)
- `rating`
- `comment`

**Relationships:**

- A review is made by a user for a property (N:1).

---

### 💳 Payments

Represents payments made for bookings.

**Key Fields:**

- `id` (Primary Key)
- `booking_id` (Foreign Key to Bookings)
- `payment_date`
- `amount`
- `status`

**Relationships:**

- A payment is linked to one booking (1:1).

## 🧩 Feature Breakdown

This Airbnb Clone project replicates the core functionalities of the Airbnb platform. Below is a detailed breakdown of each major feature and its purpose within the application.

---

### 👤 User Management

Handles user registration, login, and authentication. Users can create accounts as guests or hosts, manage their profiles, and securely access the platform.

---

### 🏠 Property Management

Enables hosts to list, edit, and manage their properties. Each listing includes details like title, description, location, price, and availability, making it searchable by users.

---

### 📆 Booking System

Allows users to book available properties for selected dates. It manages date availability, prevents overlapping reservations, and calculates the total cost of the booking.

---

### ⭐ Reviews and Ratings

Guests can leave reviews and ratings after completing a stay. This feature builds trust and transparency between users and helps others evaluate listings.

---

### 💳 Payments

Facilitates secure payment processing for bookings. Users can pay for their reservations, and hosts receive confirmation once payments are completed.
