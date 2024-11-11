# Use Node.js v10 as the base image
FROM node:10

# Set the working directory inside the container
WORKDIR /usr/src/lafs

# Copy package.json and package-lock.json files to the container
COPY package*.json ./

# Install project dependencies
RUN npm install

# Copy the entire backend project into the container
COPY . .

# Expose port 3000 for the backend API
EXPOSE 3000

# Command to start the Node.js server
CMD ["node", "server/server.js"]
