Assignment: Dockerize and Deploy Express.js App 

Using Docker Compose with Nginx

🔗 Repository to Use:
https://github.com/roy35-909/Module-3-deployment
This repository contains a simple Express.js server.

Objectives:

Your task is to containerize this Express.js app and run it alongside Nginx using Docker Compose. You will:

Dockerize the Node.js (Express) app.

Create a docker-compose.yml file that:

Just Runs a Nginx image.

Builds and runs the Express.js app from the Dockerfile.

Starts the Express app after Nginx.

Expose the application on port 8080.

Use Docker Compose to run everything.

Verify it's working in the browser.

## Prerequisites

- Node Version 22


### 1. For Run This Applications
```bash
# install packages
npm install 

# Testing The Applications
npm check

# For Run the application
npm start
```


### Deployment Process
1. **Cleanup**: Removes existing process if running
   ```bash
   pm2 delete node-app || true
   ```

2. **Start Application**: Launches with absolute path
   ```bash
   pm2 start "./src/server.js" --name node-app
   ```

3. **Save Process List**: Persists PM2 configuration
   ```bash
   pm2 save
   ```

### About The Applications
1. **Route**: This Application has 2 route
   ```bash
   / # this will show a hello world page
   ```
      ```bash
   /api # this will response a json
   ```

2. **Default Port**: By Default this application will run on port 3000

### about the project :
# Module 5 Project

This project Dockerizes a Node.js (Express) application and serves it using Nginx and Docker Compose. The app is accessible at `http://localhost:8080`.
# obective:
 task is to containerize this Express.js app and run it alongside Nginx using Docker Compose. You will:

Dockerize the Node.js (Express) app.

Create a docker-compose.yml file that:

Just Runs a Nginx image.

Builds and runs the Express.js app from the Dockerfile.

Starts the Express app after Nginx.

Expose the application on port 8080.

Use Docker Compose to run everything.

Verify it's working in the browser.
## Structure

- `Dockerfile`: Builds the Node.js app.
- `docker-compose.yml`: Runs Express app and Nginx together.
- `nginx/default.conf`: Nginx reverse proxy setup.
- `src/server.js`: Express app.
- `public/index.html`: Frontend page.

## How to Run

```bash
docker compose up --build
config nginx
create dockerfile




