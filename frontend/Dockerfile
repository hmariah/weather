# Use node.js
FROM node:boron

# Set the working directory to /app
WORKDIR /frontend

# Copy the current directory contents into the container at /backend
ADD . /frontend

# Install app dependencies
COPY package.json /frontend
RUN npm install

# Make port 9000 available to the world outside this container
EXPOSE 9000

# Define environment variable
ENV ENDPOINT "http://api.openweathermap.org/data/2.5"

# Run app.py when the container launches
CMD ["npm", "start"]