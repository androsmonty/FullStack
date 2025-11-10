# FullStack Project Documentation

## Overview

This is a full-stack web application template that demonstrates a complete project structure with separated frontend and backend components.

## Architecture

### Frontend
- **Technology**: HTML, CSS, JavaScript
- **Framework**: Bootstrap 4
- **Purpose**: User interface and presentation layer

### Backend
- **Technology**: Node.js
- **Framework**: Express.js
- **Purpose**: API server and business logic

## Project Setup

### Initial Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/androsmonty/FullStack.git
   cd FullStack
   ```

2. **Install Frontend Dependencies**
   ```bash
   cd frontend
   npm install
   cd ..
   ```

3. **Install Backend Dependencies**
   ```bash
   cd backend
   npm install
   cd ..
   ```

## Running the Application

### Start Backend Server
```bash
cd backend
npm start
```
The API will be available at `http://localhost:3000`

### Start Frontend Server
```bash
cd frontend
npm start
```
The frontend will be available at `http://localhost:8080`

## Development Workflow

### Frontend Development
1. Make changes to `frontend/index.html` or other frontend files
2. The server will automatically serve the updated files
3. Refresh browser to see changes

### Backend Development
1. Use `npm run dev` to start the server with nodemon
2. Make changes to `backend/server.js` or add new route files
3. Server will automatically restart on file changes

## Adding New Features

### Adding a New API Endpoint

1. Open `backend/server.js`
2. Add a new route:
   ```javascript
   app.get('/api/new-endpoint', (req, res) => {
     res.json({ message: 'New endpoint' });
   });
   ```

### Adding Frontend Pages

1. Create a new HTML file in the `frontend` directory
2. Link to it from `index.html` or access directly

## Testing

### Manual Testing
- Frontend: Open `http://localhost:8080` in your browser
- Backend: Use tools like Postman or curl to test API endpoints

### Example API Test
```bash
curl http://localhost:3000/health
```

## Deployment

### Production Build

For production deployment, consider:
- Using environment variables for configuration
- Setting up a process manager like PM2 for the backend
- Serving frontend through a CDN or web server like Nginx
- Implementing proper error logging and monitoring

## Troubleshooting

### Common Issues

1. **Port Already in Use**
   - Change the PORT in backend or frontend configuration
   - Kill the process using the port

2. **Module Not Found**
   - Run `npm install` in the respective directory

3. **CORS Errors**
   - Ensure the backend has CORS enabled (already configured)

## Contributing

When contributing to this project:
1. Create a new branch for your feature
2. Make your changes
3. Test thoroughly
4. Submit a pull request

## License

MIT License - See LICENSE file for details
