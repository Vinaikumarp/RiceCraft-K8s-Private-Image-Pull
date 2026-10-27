# Food Delivery – Kubernetes Deployment

## Project Description

This project demonstrates the deployment of a food delivery application on Kubernetes using containerization and Kubernetes orchestration features. It focuses on deploying application containers, managing replicas, configuring environment variables, securing credentials using Kubernetes Secrets, and exposing the application through a LoadBalancer Service.

## Technologies Used

- **Docker** – Containerization
- **Docker Hub** – Container image repository
- **Kubernetes** – Container orchestration
- **Deployments** – Application replica management
- **StatefulSets** – Managing Pods with stable identities
- **Services** – Exposing applications inside and outside the cluster
- **ConfigMaps** – Managing application configuration
- **Secrets** – Managing sensitive information
- **Resource Requests and Limits** – Managing CPU and memory allocation

## Key Features

- Deployed application containers using Kubernetes manifests.
- Configured multiple replicas for application availability.
- Pulled private Docker Hub images using `imagePullSecrets`.
- Managed application configuration using ConfigMaps.
- Injected sensitive values through Kubernetes Secrets.
- Exposed the application using a LoadBalancer Service.
- Configured CPU and memory requests and limits.
- Monitored Pod status, application events, and resource utilization using `kubectl`.

## Deployment Workflow

1. Build and push the Docker image to Docker Hub.
2. Create the Kubernetes namespace.
3. Configure the Docker Hub authentication Secret.
4. Create ConfigMaps and application Secrets.
5. Deploy the application using Kubernetes YAML manifests.
6. Expose the application through a Kubernetes Service.
7. Verify Pod health and monitor resource usage.

## Useful Commands

#create secret by using command
kubectl create secret docker-registry dockerhub-secret --docker-username=<username> --docker-password=<GitHub-Access-Token> -n dev

#create namespace for using command
kubectl create ns dev

kubectl apply -f configmap.yml
kubectl apply -f secret.yml
kubectl apply -f deploy.yml
kubectl apply -f service.yml

kubectl get pods -n dev
kubectl get deployments -n dev
kubectl get statefulsets -n dev
kubectl get services -n dev
kubectl top pods -n dev
kubectl top nodes

## Learning Outcomes

- Understanding Kubernetes application deployment and orchestration.
- Managing application configuration and credentials.
- Working with private container registries.
- Understanding Deployments, StatefulSets, and Services.
- Monitoring cluster resources and troubleshooting deployment issues.

## Author

**Vinay Kumar**

DevOps | Docker | Kubernetes | AWS | CI/CD
