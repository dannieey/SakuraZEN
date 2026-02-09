# Japanese Restaurant API 

A comprehensive backend solution for a Japanese restaurant, featuring secure authentication, a dynamic menu, and a versatile order processing system.

## Setup Instructions

1. **Install Dependencies**: Run `npm install` to install all required packages.
2. **Environment Configuration**: Create a `.env` file in the root directory and add your `MONGO_URI` and `JWT_SECRET`.
3. **Seed Database**: Run `npm run seed` to populate the menu with initial dishes.
4. **Launch Server**: Start the development server using `npm run dev`.

## API Documentation

### Authentication

* **POST /api/auth/register**: Create a new user account with username, email, and password.
* **POST /api/auth/login**: Authenticate user and receive a JWT Token for private requests.

### Menu Items

* **GET /api/menu**: Retrieve the full list of available authentic Japanese dishes.
* **GET /api/menu/:id**: Get detailed information about a specific menu item.

### Orders (Private - Requires Bearer Token)

* **POST /api/orders**: Place a new order. Supports both **Delivery** (with item list) and **Table Booking** (with date and guests).
* **GET /api/orders/myorders**: View the order history for the currently logged-in user.

## 🛠 Tech Stack

* **Runtime**: Node.js
* **Framework**: Express.js
* **Database**: MongoDB & Mongoose
* **Security**: JSON Web Tokens (JWT) & BcryptJS for password hashing
* **Development**: Nodemon & Dotenv

---

### Project Structure

* `/models`: Mongoose schemas defining the data structure for Users, Menu, and Orders.
* `/controllers`: Logical handlers that process API requests and interact with the database.
* `/middleware`: Security layer for JWT verification and route protection.
* `/routes`: Defined API endpoints and their associated controller functions.

---

