# Use the official Node.js image as the base image
FROM node:14
# Set the working directory inside the container
WORKDIR /app
# Copy the server code to the working directory
COPY server /app/server
# Change to the server directory
WORKDIR /app/server

# Install the server dependencies
RUN npm install

# Change back to the app directory
WORKDIR /app

# Copy the client code to the client directory
COPY client /app/client

# Change to the client directory
WORKDIR /app/client

# Install the client dependencies
RUN npm install

# Build the React application
RUN npm run build
# Change back to the app directory
WORKDIR /app
# Copy the README file to the root directory

# Expose the port that the server listens on

# Run the Node.js server when the container starts

# // # Developer: Captain DevOps, here's how to run the app:

# // # 1. Clone the repo and navigate to the server directory
# // # 2. Run 'npm install' to install server dependencies
# // # 3. Navigate to the client directory and run 'npm install' for React app dependencies
# // # 4. In the client directory, run 'npm run build' to build the React app
# // # 5. Navigate back to the server directory and run 'node server.js'

# // # This starts the Node.js server, serving the React app and providing API routes.

# // # I've been running it bare metal, but I need you to containerize it.

# // # Let me know if you need anything else.