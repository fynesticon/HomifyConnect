# HomifyConnect - Server

This is the server-side of the HomifyConnect application.  it is the backend of the HomifyConnect app. It handles API requests, manages data, and integrates with external services.

## Table of Contents

- Getting Started
  - Prerequisites
  - Installation
  - Environment Variables
- Usage
- API Endpoints
- Authentication
- Database
- Error Handling
- Testing
- Contributing
- License

## Getting Started

### Prerequisites

Before running the server, ensure you have the following software installed:

- Node.js
- npm
- MongoDB

### Installation

1. Clone this repository:

```
git clone <repository_url>
cd lodge_connect/server
```

2. Install dependencies:
`npm install`

### Environment Variables

`cp .env.example .env`

### Usage

To start the server, run the following command:
`npm start`

The server will run on port 4000 by default. You can access the API at `http://localhost:4000/HomifyConnect`

### API Endpoints

Below are the available API endpoints:

- `POST /HomifyConnect/user/register`: Register a new user
- `POST /HomifyConnect/user/login`: User login
- `GET /HomifyConnect/apartment`: Get all apartments with optional filters
- `GET /HomifyConnect/apartment/:id`: Get a single apartment by ID
- `POST /HomifyConnect/apartment`: Create a new apartment
- `PUT /HomifyConnect/apartment/:id`: Update an apartment by ID
- `DELETE /HomifyConnect/apartment/:id`: Delete an apartment by ID
- `POST /HomifyConnect/favorite`: Add an apartment to favorites
- `DELETE /HomifyConnect/favorite/:id`: Remove an apartment from favorites
- `POST /HomifyConnect/apartment/:apartmentId/reviews`: Add a review for an apartment

For more detailed information on each endpoint, see the [API Documentation](https://documenter.getpostman.com/view/26618323/2s946bAuLs).

### Authentication

To access protected endpoints, include the JWT token in the request's `Authorization` header with the format: `Bearer <token>`. The token is obtained upon successful user login or registration.

### Database

This server uses MongoDB as the database. Make sure you have MongoDB installed and running on your machine or provide the connection URI in the .env file.

### Error Handling

Errors are handled consistently throughout the server using a custom error middleware. Error responses include the status code and a message indicating the reason for the error.

### Collaboration

- [Ekomobong Cletus Etim](https://github.com/fynesticon)
