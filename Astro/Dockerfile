# Use the official Node.js 14 image from Docker Hub
FROM node:latest

# Update npm to the latest version
RUN npm install -g npm@latest

# Create a directory where our app will be placed
RUN mkdir -p /usr/src/app

# Change directory so that our commands run inside this new directory
WORKDIR /usr/src/app

# Install Astro CLI globally in the image
RUN npm install -g astro@latest

# Generate a new Astro application using the Astro CLI
RUN npx create-astro portfolio --template minimal

# Change directory to the new application directory
WORKDIR /usr/src/app/portfolio

# Install project dependencies
RUN npm install

# Expose the port the app runs in
EXPOSE 5000

# Serve the app
CMD ["npm", "run", "start", "--", "--port", "5000", "--hostname", "0.0.0.0"]
