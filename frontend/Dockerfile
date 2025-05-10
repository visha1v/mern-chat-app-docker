# Use Node.js as the base image
FROM node:18

# Set the working directory in the container
WORKDIR /app

# Copy only package.json and package-lock.json first to leverage Docker caching
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the entire project into the container
COPY . .

# Expose the development port
EXPOSE 3000

# Start the React app
CMD ["npm", "start"]