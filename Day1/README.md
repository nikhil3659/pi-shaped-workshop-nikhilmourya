# pi-shaped-workshop-nikhilmourya
Assignment Repo for pi-shaped-workshop Docker Kubernetes 

# DAY 1
In this assignment, I have submitted two primary files: app.py, requrements.txt and a Dockerfile.

The app.py file contains a basic Flask web application that returns a simple message — "Hello from Flask" — when accessed. The application runs successfully on port 5000.

The second file, Dockerfile, is used to create a Docker image of the Flask application. The image was successfully built and pushed to Docker Hub.

You can access the image on Docker Hub using the following link:
[https://hub.docker.com/r/nikhilmourya/myapp.v1]



# Core Concept Question:
1. Why is Docker useful in building and deploying microservices for a real-world product (like an e-commerce or banking app)?

Docker helps in creating isolated environments for each service, like payment, orders, or user login. This makes the app modular and easier to manage. It also ensures the same environment across dev, test, and prod — so no “it works on my machine” issues. Teams can work independently on different services. And it becomes faster to deploy updates with less risk.

2. What is the difference between a Docker image and a container in the context of scaling a web application?

A Docker image is like a blueprint it has your code, dependencies, and setup. A container is a running version of that image. When we need to scale, we spin up more containers from the same image. So, the image stays the same, but we can run multiple containers to handle more load. It’s fast and consistent every time.

3. How does Kubernetes complement Docker when running a product at scale (e.g., hundreds of containers)?

Docker runs individual containers, but when we need to manage many containers across servers, Kubernetes steps in. It helps with auto-scaling, load balancing, and restarting failed containers. Kubernetes also makes deployments easier with features like rolling updates. It basically acts like a container manager when things get big.
