# ToDo Application – Dockerized

## Docker Hub Repository

https://hub.docker.com/repository/docker/a1exic/litvinov/general

Docker image tag:
<your-dockerhub-username>/todoapp:1.0.0

---

# Build and Push Instructions

## 1. Login to Docker Hub

docker login

## 2. Build the Docker image

docker build -t todoapp:1.0.0 .

## 3. Tag the image for Docker Hub

docker tag todoapp:1.0.0 <a1exic/litvinov>/todoapp:1.0.0

## 4. Push the image to Docker Hub

docker push <a1exic/litvinov>/todoapp:1.0.0

---

# Run the application

## Option 1: Run locally built image

docker run -p 8080:8080 todoapp:1.0.0

## Option 2: Run image directly from Docker Hub

docker run -p 8080:8080 <a1exic/litvinov>/todoapp:1.0.0

---

# Access the Application

After running the container with:

docker run -p 8080:8080 <a1exic/litvinov>/todoapp:1.0.0

Open a browser and navigate to:

http://localhost:8080

If running on a remote machine, open:

http://<host-ip>:8080

---

# Verification

The application starts inside the container without errors.
Database migrations are executed during image build.
The server runs on:

0.0.0.0:8080
