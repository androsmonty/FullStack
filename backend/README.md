# Backend

This is the backend API for the FullStack project, built with Node.js and Express.

## Features

- RESTful API endpoints
- CORS enabled for cross-origin requests
- JSON response format
- Health check endpoint
- Error handling middleware

## API Endpoints

### GET /
Returns API information and available endpoints.

**Response:**
```json
{
  "message": "Welcome to FullStack API",
  "version": "1.0.0",
  "endpoints": {
    "health": "/health",
    "api": "/api"
  }
}
```

### GET /health
Health check endpoint to verify server status.

**Response:**
```json
{
  "status": "OK",
  "timestamp": "2025-11-10T23:54:00.000Z"
}
```

### GET /api/data
Returns sample data.

**Response:**
```json
{
  "data": [
    { "id": 1, "name": "Item 1" },
    { "id": 2, "name": "Item 2" },
    { "id": 3, "name": "Item 3" }
  ]
}
```

## Getting Started

### Installation

```bash
npm install
```

### Running the Server

```bash
npm start
```

The server will start on `http://localhost:3000`

### Development Mode

```bash
npm run dev
```

This will start the server with nodemon for automatic restarts on file changes.

## Environment Variables

- `PORT` - Server port (default: 3000)

## Dependencies

- express - Web framework
- cors - CORS middleware

## Dev Dependencies

- nodemon - Auto-restart on file changes
