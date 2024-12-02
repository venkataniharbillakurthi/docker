# React Js  Deployed with Docker

# Docker fie commands
## Step 1: Use a Node.js image to build the app
FROM node:16 as build

## Step 2: Set working directory in the container
WORKDIR /app

## Step 3: Copy package.json and package-lock.json to install dependencies
COPY package.json package-lock.json ./

## Step 4: Install dependencies
RUN npm install

## Step 5: Copy the rest of the application code
COPY . .

## Step 6: Build the application
RUN npm run build

## Step 7: Use an Nginx image to serve the built files
FROM nginx:alpine

## Step 8: Copy the built React files to the Nginx directory
COPY --from=build /app/build /usr/share/nginx/html

## Step 9: Copy custom Nginx configuration to handle React routing
COPY nginx.conf /etc/nginx/conf.d/default.conf

## Step 10: Expose the container port
EXPOSE 80

## Step 11: Start Nginx server
CMD ["nginx", "-g", "daemon off;"]



# Docker Container commands
Container Commands
docker run hello-world - Runs the Hello World application.
docker ps - Lists running containers.
docker ps -a - Lists all containers (past and present).
docker stop - Stops a running container.
docker rm - Removes a container.

# 1. Log in to Docker Hub
Run the following command in your terminal:
docker login

# 2. Tag Your Docker Image
docker tag my-task-react-app venkataniharbillakurthi/reactproject/my-task:latest

# 3. Push the Image to Docker Hub
Push the image to Docker Hub using:
docker push venkataniharbillakurthi/reactproject/my-task:latest
# 5. Share the Image
Share the image name with others. For example:
venkataniharbillakurthi/reactproject/my-task:latest
# 6. Others can pull the image using:
docker pull yourusername/reactproject/my-task:latest

# http://localhost:8080/


