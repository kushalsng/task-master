# Use the official Node.js image as base
FROM node:18-alpine

# Set the working directory in the container
WORKDIR /taskmaster

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Expose the port that the client will run on
EXPOSE 3000

# Command to run the application
CMD ["npm", "start"]
