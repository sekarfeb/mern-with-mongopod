# Use an official Node.js runtime as the base image
FROM node:14

# Set the working directory in the container
WORKDIR /app

# Copy the package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install project dependencies
RUN npm install

# Install nodemon globally
RUN npm install -g nodemon

# Copy the source code to the working directory
COPY . .

# Expose the port on which the backend server will run
EXPOSE 5000

# Start the backend server using nodemon
CMD ["nodemon", "server.js"]
