# Use NodeJS base image
#FROM node:13
FROM node:13

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Copy all other files
COPY ./ /usr/src/app/

# Install dependencies
RUN npm install .

# Copy app source
COPY . .

# Bind the port that the image will run on
EXPOSE 8080

# Define the Docker image's behavior at runtime
CMD ["npm", "run", "dev", "--external"]
#ENTRYPOINT ["/bin/bash", "./run.sh"]
