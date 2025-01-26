## Overview
This is the backend of the e-commerce platform, built using Node.js, Express.js, and MongoDB. It handles the server-side logic for user authentication, product management, order processing, and integration with third-party services such as Cloudinary for image storage and a payment gateway for secure transactions.

## Features
- **User Authentication**: Secure JWT-based authentication for users and admins.
- **Product Management**: API endpoints for creating, updating, deleting, and listing products.
- **Order Management**: Handling user orders, including creation, updating, and tracking.
- **Cloudinary Integration**: Upload and manage product images via Cloudinary.
- **Admin Panel**: Endpoints for managing products, users, and orders by the admin.

## Technologies Used
- **Node.js**: JavaScript runtime for server-side logic.
- **Express.js**: Web framework for building RESTful APIs.
- **MongoDB**: NoSQL database for storing user data, products, and orders.
- **Mongoose**: ODM (Object Document Mapper) for MongoDB to simplify data interactions.
- **JWT (JSON Web Tokens)**: Authentication method for securing routes.
- **Cloudinary**: Image storage and management service for product images.
- **Bcrypt.js**: For password hashing.
- **dotenv**: For managing environment variables.

## API Endpoints
- **POST** `/api/signup` - Register a new user.
- **POST** `/api/signin` - Log in and get a JWT token.
- **POST** `/api/userLogout` - Log out the current user.
- **GET** `/api/get-product` - Get a list of all products.
- **POST** `/api/upload-product` - Add a new product (admin only).
- **POST** `/api/update-product` - Update a product (admin only).
- **GET** `/api/all-user` - Get all users (admin only).
- **POST** `/api/delete-cart-product` - deleteCartProduct.
- **POST** `/api/filter-product` - filterProduct.


## Installation
To set up the backend locally:

1. Clone the repository:

2. Install dependencies:
   ```
   cd ecommerce-backend
   npm install
   ```

3. Set up environment variables:
   - Create a `.env` file in the root directory with the following variables:
     - `PORT=8080`
     - `MONGODB_URI=<your_mongo_connection_string>`
     - `JWT_SECRET=<your_jwt_secret>`
     - `CLOUDINARY_URL=<your_cloudinary_url>`
     - `PAYMENT_GATEWAY_SECRET=<your_payment_gateway_secret>`
     - (Other variables for services you use)

4. Run the server:
   ```
   npm start
   ```

5. The server will be running at `http://localhost:8080`.

## Contributing
1. Fork this repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Submit a pull request.

