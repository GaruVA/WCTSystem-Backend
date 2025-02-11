# WCTSystem-Backend

This repository hosts the backend server for the **WCTSystem** application, a waste collection tracking system for urban areas.

## Prerequisites

Ensure you have the following installed on your machine before setting up the project:

- **Node.js** (v14 or later)
- **npm** (Node Package Manager)
- A **MongoDB Atlas** account for database management

## Getting Started

Follow these steps to set up the project locally:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/GaruVA/wctsystem-backend.git
   cd wctsystem-backend
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Environment configuration**:
   - Create a .env file in the root directory: type nul > .env
   - Include the following content in the .env file:
      ```env
      MONGODB_URI=<mongodb-uri>
      PORT=5000
      JWT_SECRET=<jwt-secret>
      ```
   - Replace `<mongodb-uri>` and `<jwt-secret>` with your actual MongoDB connection string and JWT secret.

4. **Start the development server**:
   ```bash
   npm run dev
   ```

   The backend server should now be running at `http://localhost:5000`.

## Available Scripts

- **`npm run dev`**: Starts the development server with hot-reloading using `ts-node-dev`.
- **`npm run build`**: Compiles the TypeScript code into JavaScript, generating the `dist` folder.
- **`npm start`**: Runs the production server using the compiled JavaScript files.

## API Endpoints

- **Authentication**
  - `POST /api/auth/register`: Register a new user.
  - `POST /api/auth/login`: Log in an existing user.

- **Bins**
  - `POST /api/bins/update`: Update bin data.
  - `GET /api/bins`: Fetch all bin statuses.
