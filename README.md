# Packers_n_Movers

## Overview
Packers_n_Movers is an advanced web application designed to simplify packers and movers services. This enhanced version of the initial `Pack_n_Move` project is built using React.js, Node.js, and MySQL, providing an intuitive user interface and powerful backend functionalities. The platform allows users to search for services based on their desired `from` and `to` locations, compare companies by ratings and prices, and book services seamlessly.

---

## Features
1. **User Authentication**
   - Login and Registration functionality.
   - User profile management.
2. **Service Search**
   - Search services based on `from` and `to` locations.
3. **Dynamic Cost Calculator**
   - Estimate the cost of the service based on distance and weight.
4. **Company Comparison**
   - View company details, including ratings, prices, and availability.
5. **Service Booking**
   - Book a service after comparing options.
6. **Feedback System**
   - Users can leave feedback for services.
7. **Chat Assistant**
   - Interact with a chatbot for queries related to the application.
8. **Admin Panel**
   - View booking history.
   - Cancel bookings.
   - Manage companies.
   - Respond to user feedback.

---

## Technologies Used
- **Frontend**: React.js
- **Backend**: Node.js
- **Database**: MySQL

---

## Installation Guide

### Prerequisites
- Node.js and npm
- MySQL Database
- IDE (e.g., Visual Studio Code)

## Usage Instructions

1. **User Workflow**
   - Register or log in to the platform.
   - Use the search feature to select your `from` and `to` locations.
   - Utilize the Dynamic Cost Calculator to estimate service costs.
   - Browse companies, compare ratings and prices.
   - Choose a company, book the service, and leave feedback after completion.
   - Interact with the Chat Assistant for any queries.

2. **Admin Workflow**
   - Log in to the admin panel.
   - View and manage booking history.
   - Approve, cancel, or update bookings.
   - View and manage companies.
   - Respond to user feedback.

---

## Database Schema
### Table: `users`
| Field     | Type         | Description         |
|-----------|--------------|---------------------|
| id        | INT          | Auto-increment ID  |
| username  | VARCHAR(255) | User's name        |
| email     | VARCHAR(255) | User's email       |
| password  | VARCHAR(255) | User's password    |

### Table: `bookings`
| Field         | Type          | Description                |
|---------------|---------------|----------------------------|
| booking_id    | INT           | Auto-increment booking ID |
| user_id       | INT           | User ID (foreign key)     |
| from_location | VARCHAR(255)  | Starting location         |
| to_location   | VARCHAR(255)  | Destination location      |
| company_id    | INT           | Selected company ID       |
| status        | ENUM('Pending','Approved','Cancelled') | Booking status |

### Table: `companies`
| Field         | Type          | Description                |
|---------------|---------------|----------------------------|
| company_id    | INT           | Auto-increment company ID |
| name          | VARCHAR(255)  | Company name              |
| rating        | DECIMAL(3,2)  | Average company rating    |
| price         | DECIMAL(10,2) | Price for services        |
| location      | VARCHAR(255)  | Company location          |

### Table: `feedback`
| Field         | Type          | Description                |
|---------------|---------------|----------------------------|
| feedback_id   | INT           | Auto-increment feedback ID|
| user_id       | INT           | User ID (foreign key)     |
| message       | TEXT          | Feedback message          |
| date          | DATETIME      | Feedback date             |

---

## Future Enhancements
- Integration of payment gateways.
- Real-time location tracking for services.
- Advanced analytics for user preferences.

---


