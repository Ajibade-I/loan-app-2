# Loan App

This is a loan application built with Node.js and Express.js.

## Installation

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.

## Usage

1. Start the server: `npm start`.
2. To run in development mode with auto-restart: `npm run dev`.
3. To import data: `npm run data:import`.
4. To destroy data: `npm run data:destroy`.

## Features

- **Authentication and Authorization:** Secure user authentication using JWT ensures controlled access to the application.
- **Error Handling:** Comprehensive error management with custom messages enhances the user experience.
- **Middleware:** Leveraging Express.js middleware like `cookie-parser`, `cors`, and `express-session` for enhanced security and performance.
- **Validation:** Integration of Yup schema validation maintains data integrity and enforces input validation rules.
- **Database:** MongoDB with Mongoose for data storage and manipulation.
- **Password Encryption:** User passwords are encrypted using `bcryptjs` to ensure secure storage.
- **Email Notification:** Seamless email notifications powered by `nodemailer` for user account activation, password reset, and confirmation.
- **Loan Management:** Users can create accounts, request loans, fund accounts, manage loan requests, and refund loans.

## Tech Stack

- Node.js
- Express.js
- MongoDB
- JWT (JSON Web Tokens)
- bcryptjs
- nodemailer
- Yup (Schema Validation)
- HTTP Status Codes

## Endpoints

### Account Endpoints

- **POST /account:** Create account (private/admin).
- **GET /account/:id:** Get account (private/admin).
- **POST /account/:id/fund:** Fund account (private/admin).
- **PUT /account/:id:** Update account (private/admin).

### Authentication Endpoints

- **POST /auth/signup:** User signup (public).
- **POST /auth/login:** User login (public).

### Signup Code Endpoints

- **POST /codes:** Create signup code (private/admin).
- **GET /codes:** Get all signup codes (private/admin).
- **DELETE /codes/:id:** Delete a signup code (private/admin).

### Loan Endpoints

- **GET /loans:** Get all loan requests (private/admin).
- **POST /loans/:loanId/action:** Admin accept or decline loan (private/admin).
- **POST /loans/:loanId/refund:** User loan refund (private).

### Transaction Endpoints

- **GET /transactions:** Get all transactions (private/admin).
- **GET /transactions/:id:** Get transaction (private).
- **GET /transactions/overview/all:** Get transaction overview (private).

### User Endpoints

- **GET /users:** Get all users (private/admin).
- **GET /users/:id/profile:** User profile (private).
- **POST /users/:userId/request-loan:** Make loan request (private).
- **GET /users/:userId/loan-requests:** Get user requests (private).
- **GET /users/:userId/transactions:** Get user transactions (private).

## Environment Variables

- `MONGO_URI`: MongoDB connection URI.
- `JWT_PRIVATE_KEY`: Private key used for JWT token generation.
- `ACCOUNT_ID`: MongoDB Account Model objectID.
- `CLIENT_URL`: URL of the client application.
- `NODE_ENV`: Environment mode (development, production, etc.).

## Contributors

- [Ajibade Isiaka](https://github.com/Ajibade-I)
