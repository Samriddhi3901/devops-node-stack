# DevOps Node Stack

Containerized Node.js app with Express, built for MongoDB integration. Uses Docker volumes for data persistence and networking for API access on port 3002.

## Overview

This project demonstrates a containerized Node.js application using Docker for deployment and MongoDB for data storage. The application is built with Express.js and configured to run on port 3002.

## Features

- **Node.js & Express**: RESTful API server
- **MongoDB Integration**: Database connectivity for data persistence
- **Docker Containerization**: Fully containerized application
- **Volume Mounting**: Persistent data storage using Docker volumes
- **Network Configuration**: Proper Docker networking for service communication

## Prerequisites

- Docker
- Docker Compose
- Node.js (for local development)

## Quick Start

### Using Docker

1. **Clone the repository**
   ```bash
   git clone https://github.com/Samriddhi3901/devops-node-stack.git
   cd devops-node-stack
   ```

2. **Build and run with Docker Compose**
   ```bash
   docker-compose up -d
   ```

3. **Access the application**
   ```
   http://localhost:3002
   ```

### Local Development

1. **Install dependencies**
   ```bash
   npm install
   ```

2. **Start MongoDB (if running locally)**
   ```bash
   mongod
   ```

3. **Run the application**
   ```bash
   npm start
   ```

## Docker Configuration

### Services
- **Node.js App**: Express server running on port 3002
- **MongoDB**: Database service with persistent volume

### Volumes
- Data persistence for MongoDB
- Application code mounting for development

### Networking
- Internal Docker network for service communication
- Port mapping for external access

## API Access

The application exposes APIs on port 3002:
```
http://localhost:3002/api/...
```

## MongoDB Integration

The application connects to MongoDB for:
- Data storage
- CRUD operations
- Persistent data management

## Project Structure

```
devops-node-stack/
├── Dockerfile
├── docker-compose.yml
├── package.json
├── server.js
└── ...
```

## Environment Variables

Configure the following environment variables:
- `PORT`: Application port (default: 3002)
- `MONGODB_URI`: MongoDB connection string
- `NODE_ENV`: Environment mode

## Commands

### Docker Commands
```bash
# Build image
docker build -t devops-node-stack .

# Run container
docker run -p 3002:3002 devops-node-stack

# Stop containers
docker-compose down

# View logs
docker-compose logs
```

### Development Commands
```bash
# Install dependencies
npm install

# Start server
npm start

# Development mode
npm run dev
```

## License

This project is open source and available under the [MIT License](LICENSE).
