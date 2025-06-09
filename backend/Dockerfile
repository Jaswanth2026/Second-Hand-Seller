# Use Node.js LTS as base image
FROM node:18

# Set working directory inside container
WORKDIR /app

# Copy backend package.json files and install backend dependencies only
COPY backend/package*.json ./backend/
RUN cd backend && npm install

# Copy backend source code
COPY backend/ ./backend/

# Copy frontend build (already built by pipeline)
COPY Frontend/build ./frontend/build

# Set environment variables
ENV PORT=4000
ENV NODE_ENV=production

# Expose the port
EXPOSE 4000

# Set working directory to backend for running the app
WORKDIR /app/backend

# Run the backend server
CMD ["node", "server.js"]
