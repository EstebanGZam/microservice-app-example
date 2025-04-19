# Use Node.js 8.17.0 as the base image for building the application.
# This image includes Node.js and npm, which are necessary for running the application.
FROM node:8.17.0

# Set the working directory inside the container to /app
# All subsequent commands will be executed from this directory.
WORKDIR /app

# Copy the entire contents of the current directory (the application's source code) into the /app directory in the container
COPY . .

# Install the Node.js dependencies specified in package.json
# This command reads the package.json file and installs the necessary npm packages.
RUN npm install

# Build the application
# This command runs the `build` script defined in package.json, typically used to compile and prepare the application for production.
RUN npm run build

# Define the command to start the application
# This command will be executed when the container starts.
# It runs the `start` script defined in package.json to launch the application.
CMD ["npm", "start"]
