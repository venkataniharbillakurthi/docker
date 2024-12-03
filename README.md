# react js Website Deployed with Docker
This project demonstrates the deployment of a static website using Docker. The website includes HTML, CSS, JavaScript files and React js, served through a lightweight Nginx web server.

## Deployment Steps

### 1. Prepare the Dockerfile

FROM nginx:alpine    

COPY . /usr/share/nginx/html    

EXPOSE 80

### 2. Build the Docker image

docker build -t reactproject-website .    

### 3. Run the Docker container

docker run -d -p 8080:80 reactproject-website

* //-d: Runs the container in detached mode.
* //-p 8080:80: Maps port 80 of the container to port 8080 on our machine.


## This website is now deployed and can be accessed locally or through a Docker-enabled environment. Visit http://localhost:8080 to view it.
