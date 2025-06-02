# Use the official Node.js LTS Alpine image for a lightweight build
FROM node:18-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to install dependencies
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of your application code
COPY . .

# Expose the port your app runs on
EXPOSE 4000

# Define the command to run your app
CMD ["npm", "start"]

