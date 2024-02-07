# Reddit Clone on Kubernetes with Ingress

This repository guides you through deploying a Reddit clone on Kubernetes with Ingress for streamlined external access.

## Prerequisites

- EC2 instance (AMI: Ubuntu, Type: t2.medium)
- Docker
- Minikube
- kubectl

## Step-by-Step Guide

1. **Clone Source Code:**
   - Use `git clone` to fetch the Reddit clone application source code.

2. **Containerize the Application:**
   - Write a Dockerfile to set up the environment, copy code, install dependencies, expose port 3000, and start the app.

3. **Build and Push Docker Image:**
   - Build the Docker image using `docker build`.
   - Push the image to DockerHub with `docker push`.

4. **Write Kubernetes Manifest Files:**
   - Create `Deployment.yml` and `Service.yml` files specifying deployment and service configurations.

5. **Deploy to Kubernetes:**
   - Apply deployment and service files with `kubectl apply`.

6. **Configure Ingress:**
   - Write an `Ingress.yml` file defining rules for routing external traffic to Kubernetes services.

7. **Enable Ingress in Minikube:**
   - If using Minikube, enable Ingress with `minikube addons enable ingress`.

8. **Apply Ingress Settings:**
   - Apply Ingress settings to Kubernetes using `kubectl apply`.

9. **Verify Ingress:**
   - Check the status of the Ingress resource with `kubectl get ingress`.

10. **Expose the App:**
    - Expose the deployment with `kubectl expose deployment`.

11. **Port Forwarding:**
    - Expose the app service using `kubectl port-forward`.

12. **Test Ingress:**
    - Test the Ingress with `curl` commands.

13. **Access the Application:**
    - View the deployed application on `EC2_ip:3000`. Ensure port 3000 is open in the EC2 security group.

Congratulations on successfully deploying the Reddit clone on Kubernetes with Ingress!