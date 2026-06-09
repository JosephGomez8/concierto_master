# 🎵 Concierto Master

## Project Overview

Concierto Master is a web application developed with Laravel for concert management and administration. It allows ticket sales and reservations, user administration, revenue tracking, and automatic generation of electronic tickets.

The system centralizes all processes related to organizing musical events, providing a secure and efficient platform for both customers and administrators.

---

# Project Objective

To automate concert management and ticket sales through a web application that enables administrators to manage reservations, sales, revenues, users, and electronic ticket generation.

---

# Main Features

* User and role management
* Individual and bulk ticket sales
* Seat reservation system
* Automatic PDF ticket generation
* Ticket delivery via email
* Reservation lookup
* Revenue management
* Administrative dashboard
* Seat availability control
* Buyer management

---

# System Architecture

The project follows the **MVC (Model-View-Controller)** architectural pattern provided by Laravel.

## Models

The main entities of the system include:

* User
* UserGmo
* Buyer
* Seat
* SeatSold
* Collection

## Controllers

Business logic is handled by:

* UserController
* SeatController
* SeatSoldController
* CollectionController

## Views

The graphical user interface includes modules for:

* Customers
* Administrators
* Sales management
* Reservation lookup
* Revenue control

---

# System Modules

## User Management

Allows administrators to:

* Create users
* Edit user information
* Delete users
* Manage permissions
* Control system access

### Main Functions

* User registration
* Login
* Logout
* Profile management

---

## Seat Management

Provides functionality to:

* Register seats
* Check availability
* Assign seats to buyers
* Manage occupancy

### Main Entity

```text
Seat
```

---

## Sales Management

Provides functionality for:

* Individual ticket sales
* Bulk ticket sales
* Transaction registration
* Availability control

### Main Entity

```text
SeatSold
```

---

## Buyer Management

Stores customer information associated with ticket purchases.

### Recorded Information

* Full name
* Identification number
* Email address
* Purchase details

### Main Entity

```text
Buyer
```

---

## Ticket Management

The system automatically generates electronic tickets for every completed purchase.

### Features

* PDF ticket generation
* Ticket download
* Ticket delivery via email
* Individual and bulk ticket generation

---

## Revenue Management

Provides financial control over ticket sales.

### Features

* Revenue registration
* Revenue tracking
* Revenue record deletion
* Income monitoring

### Main Entity

```text
Collection
```

---

# System Workflow

## 1. User Authentication

Administrators access the platform through a secure login form.

The system validates:

* Username
* Password
* Access permissions

---

## 2. User Administration

Administrators can:

* Create users
* Update user information
* Delete users
* Assign permissions

---

## 3. Reservation or Purchase

Customers select available seats for a concert.

The system:

* Verifies seat availability
* Registers the reservation
* Records the sale

---

## 4. Ticket Generation

Once the purchase is completed:

* A PDF ticket is generated
* Sale information is stored
* Ticket download becomes available
* A copy is sent by email

---

## 5. Sales Administration

Administrators can:

* Review completed sales
* View buyer information
* Access generated tickets
* Manage sales records

---

## 6. Revenue Control

Income generated from ticket sales can be tracked and managed through the revenue management module.

---

# Main System Routes

## Public Access

```text
/
```

Home page.

---

```text
/consult-reservation
```

Reservation lookup.

---

```text
/form-login
```

Login page.

---

## Administration

```text
/system/users
```

User management.

---

```text
/system/admin-sales
```

Sales administration.

---

```text
/collect-money
```

Revenue management.

---

## Tickets

```text
/system/download-ticket/{id}
```

Ticket download.

---

```text
/system/send-ticket-customer/{id}
```

Ticket delivery via email.

---

# Database

The application uses MySQL as its relational database management system.

## Main Tables

### users

Authenticated users.

### users_gmos

Administrative users.

### roles_gmos

System roles.

### buyers

Customer information.

### seats

Available seats.

### seats_sold

Sold seats.

### collections

Revenue records.

---

# Technologies Used

## Backend

* PHP 8
* Laravel 8

## Database

* MySQL

## Frontend

* HTML5
* CSS3
* JavaScript
* Bootstrap

## Tools

* Composer
* Git
* GitHub

---

# Key Dependencies

## laravel/framework

Main application framework.

## laravel/sanctum

Authentication and API security.

## barryvdh/laravel-dompdf

PDF generation.

## milon/barcode

Barcode generation.

## laravolt/avatar

Avatar generation.

---

# Project Structure

```text
concierto_master/
│
├── app/
├── bootstrap/
├── config/
├── database/
├── public/
├── resources/
├── routes/
├── storage/
├── tests/
├── composer.json
├── package.json
└── artisan
```

---

# Installation

## Clone the repository

```bash
git clone https://github.com/JosephGomez8/concierto_master.git
```

## Enter the project directory

```bash
cd concierto_master
```

## Install dependencies

```bash
composer install
```

## Configure environment variables

```bash
cp .env.example .env
```

## Generate Laravel application key

```bash
php artisan key:generate
```

## Run database migrations

```bash
php artisan migrate
```

## Start the development server

```bash
php artisan serve
```

---

# Security

The system implements:

* Authentication middleware
* Administrative access control
* User validation
* Protected administrative routes

---

# Benefits

* Automated ticket sales process
* Centralized concert management
* Efficient user administration
* Automatic ticket generation
* Financial tracking through revenue management
* Improved administrative organization

---

# Author

Academic project developed for concert ticket sales and management using Laravel

---

# Project Status

Academic project developed with Laravel for concert management and ticket sales administration.
