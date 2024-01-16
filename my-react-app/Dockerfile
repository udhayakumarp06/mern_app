# Use a base image with Node.js pre-installed
FROM node:14

# Set working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install app dependencies
RUN npm install

# Copy the entire app directory contents into the container
COPY . .

# Expose port 3000 (or the port your React app runs on)
EXPOSE 3000

# Build the React app
RUN npm run build

# Start the app
CMD ["npm", "start"]
