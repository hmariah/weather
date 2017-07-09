# Use node.js
FROM node:boron

# Set the working directory to /backend
WORKDIR /backend

# Copy the current directory contents into the container at /backend
ADD . /backend

# Install app dependencies
COPY package.json /backend
RUN npm install
RUN npm install async

# Make port 9000 available to the world outside this container
EXPOSE 9000

# Define environment variable
ENV APPID="0e40f73f70e601965769ef4d9cea028a"
ENV MAP_ENDPOINT="http://api.openweathermap.org/data/2.5"
ENV TARGET_CITY="Espoo,fi"
ENV PORT=9000

# Run it
CMD ["npm", "start"]