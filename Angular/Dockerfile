# Use the official Node.js 14 image from Docker Hub
FROM node:latest

# Create a directory where our app will be placed
RUN mkdir -p /usr/src/app

# Change directory so that our commands run inside this new directory
WORKDIR /usr/src/app

# Install Angular CLI globally in the image
RUN npm install -g @angular/cli@latest

# Generate a new Angular application using the Angular CLI
RUN ng new website

# Change directory to the new application directory
WORKDIR /usr/src/app/website

# Expose the port the app runs in
EXPOSE 4200

# Serve the app
CMD ["ng", "serve", "--host", "0.0.0.0"]