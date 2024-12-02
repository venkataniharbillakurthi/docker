# React Js  Deployed with Docker

## Docker Container
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


