# Team CSE341 Project

Collaborative backend web app built with Node.js, Express, and MongoDB.

My role focused on **database integration and CRUD operations**, ensuring reliable data persistence and efficient API endpoints.

## Features

- MongoDB database integration
- CRUD operations for authors, books, libraries, and users
- GitHub authentication with Passport
- Session support with Express Session and MongoDB
- Swagger API documentation
- Automated API tests with Jest and Supertest

## Tech Stack

- Node.js
- Express
- MongoDB and MongoDB Node.js Driver
- Passport and GitHub OAuth
- Jest and Supertest
- Swagger UI

## Getting Started

### Prerequisites

- Node.js 18 or later
- A MongoDB database
- GitHub OAuth credentials for authentication features

### Installation

```bash
npm install
```

Create a `.env` file in the project root:

```env
MONGODB_URL=your_mongodb_connection_string
SESSION_SECRET=your_session_secret
GITHUB_CLIENT_ID=your_github_client_id
GITHUB_CLIENT_SECRET=your_github_client_secret
```

Start the development server:

```bash
npm start
```

The server runs on `http://localhost:3002` by default. Set the `PORT` environment variable to use a different port.

## API Endpoints

| Resource | Endpoints |
| --- | --- |
| Authors | `GET`, `POST` `/authors`; `GET`, `PUT`, `DELETE` `/authors/:id` |
| Books | `GET`, `POST` `/books`; `GET`, `PUT`, `DELETE` `/books/:id` |
| Libraries | `GET`, `POST` `/libraries`; `GET`, `PUT`, `DELETE` `/libraries/:id` |
| Users | `GET`, `POST` `/users`; `GET`, `PUT`, `DELETE` `/users/:id` |
| Authentication | GitHub authentication under `/auth` |

User creation and deletion require authentication.

## API Documentation

Swagger documentation is available at:

```text
http://localhost:3002/api-docs
```

## Testing

Run the test suite with:

```bash
npm test
```

## Project Structure

```text
config/       Authentication configuration
controllers/  CRUD request handlers
data/         MongoDB connection setup
middleware/   Authentication and validation middleware
models/       Data models
routes/       API route definitions
tests/        Jest and Supertest API tests
```
