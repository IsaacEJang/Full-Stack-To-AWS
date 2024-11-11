# Use Node.js v10 as the base image
FROM node:10

# Set the working directory inside the container
WORKDIR /usr/src/lafs

# Copy package.json and package-lock.json files to the container
COPY package*.json ./

# Install Angular CLI and project dependencies
RUN npm install -g @angular/cli@v6-lts
RUN npm install

# Copy the entire project into the container
COPY . .

# Expose port 4200 for the frontend application
EXPOSE 4200

# Command to start the Angular app
CMD ["ng", "serve", "--host", "0.0.0.0"]
