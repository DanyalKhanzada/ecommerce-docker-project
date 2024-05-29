# Use the official Node.js image as the base image

# Set the working directory inside the container

# Copy package.json and package-lock.json to the working directory

# Install the dependencies

# Copy the rest of the application source code

# Expose the port that the microservice listens on

# Run the Node.js application when the container starts


# Use the official Node.js image as the base image
FROM node:14
# Set the working directory inside the container
WORKDIR /app
# Copy package.json and package-lock.json to the working directory
COPY package*.json .
# Install the dependencies
RUN npm install
# Copy the rest of the application source code
COPY . .
# Expose the port that the API listens on
EXPOSE 3003
# Run the Node.js application when the container starts
CMD ["node", "auth_api.js"]