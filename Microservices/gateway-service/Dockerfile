# Use an appropriate base image
FROM node:14

# Set up the working directory
WORKDIR /usr/src/app

# Handle dependencies installation
COPY package*.json ./
RUN npm install

# Copy the rest of the application code
COPY . .

# Configure the correct port
EXPOSE 8080

# Use proper CMD instructions
CMD ["node", "app.js"]
