# Use a Node.js image
FROM node:18-alpine

# Set the working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package.json ./
RUN npm install

# Copy the rest of the app
COPY . .

# Build the Astro app
RUN npm run build

# Expose the port Astro will run on
EXPOSE 3000

# Start the Astro app
CMD ["npm", "start"]
