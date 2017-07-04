# Use node.js
FROM node:boron

# Set the working directory to /frontend
WORKDIR /frontend

# Copy the current directory contents into the container at /frontend
ADD . /frontend

# Install app dependencies
COPY package.json /frontend
RUN npm install

# Make port 9000 available to the world outside this container
EXPOSE 9000
EXPOSE 8000

# Define environment variable
ENV ENDPOINT="http://api.openweathermap.org/data/2.5"

# Run it
CMD ["npm", "start"]