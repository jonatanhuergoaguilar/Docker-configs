# Use the official Node.js  image from Docker Hub
FROM node:latest

# Update npm to the latest version
RUN npm install -g npm:latest

# Create a directory where our app will be placed
RUN mkdir -p /usr/src/app 

# Change directory so that our commands run inside this new directory
WORKDIR /usr/src/app

# Generate a new React application using create-react-app
RUN npx create-vite react-app --template react-swc

# Change directory to the new application directory
WORKDIR /usr/src/app/react-app

# Install dependencies
RUN npm install

# Expose the port the app runs in
EXPOSE 3000

# Serve the app
CMD ["npm", "run", "dev"]

