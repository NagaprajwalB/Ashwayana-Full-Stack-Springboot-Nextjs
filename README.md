# Ashvayana Project

This repository contains the full-stack Ashvayana admin panel:
- Backend: Spring Boot + Java + PostgreSQL
- Frontend: Next.js + React + TypeScript

## Prerequisites

Make sure the following are installed on your machine:
- Java 21
- Node.js 20+ and npm
- PostgreSQL running locally

## 1. Backend Setup

1. Open a terminal and go to the backend folder:
   ```bash
   cd backend
   ```
2. Make sure PostgreSQL is running and a database named `ashvayana` exists.
3. Update the database credentials in the backend configuration file if needed:
   - [backend/src/main/resources/application.properties](backend/src/main/resources/application.properties)
4. Start the backend:
   - Windows:
     ```bash
     mvnw.cmd spring-boot:run
     ```
   - macOS/Linux:
     ```bash
     ./mvnw spring-boot:run
     ```
5. The backend will run at:
   ```text
   http://localhost:8081
   ```

## 2. Frontend Setup

1. Open a second terminal and go to the frontend folder:
   ```bash
   cd frontend
   ```
2. Create a `.env.local` file with the backend URL:
   ```env
   NEXT_PUBLIC_API_BASE_URL=http://localhost:8081/api
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Start the frontend development server:
   ```bash
   npm run dev
   ```
5. Open the app in your browser:
   ```text
   http://localhost:3000
   ```

## 3. Default Configuration Notes

- Backend port: `8081`
- Frontend port: `3000`
- Default PostgreSQL settings in the project are:
  - username: `postgres`
  - password: `postgres`
  - database: `ashvayana`

## 4. Optional Notes

If image upload features are used, Cloudinary credentials may also need to be configured in the backend properties file.
