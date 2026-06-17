# DevOps Demo

A simple DevOps project built with Spring Boot, Maven, Docker, GitHub Actions, Docker Hub, and Kubernetes.

## Project Overview

This project demonstrates a complete DevOps workflow:

1. Develop a Spring Boot REST API
2. Build the application using Maven
3. Containerize the application with Docker
4. Automate builds using GitHub Actions
5. Publish Docker images to Docker Hub
6. Deploy the application to Kubernetes

## Technologies Used

- Java 17
- Spring Boot 3.5
- Maven
- Git & GitHub
- GitHub Actions
- Docker
- Docker Hub
- Kubernetes

## Application Endpoint

### Hello Endpoint

```http
GET /hello
```

Response:

```text
Hello DevOps!
```

Example:

```bash
curl http://localhost:8080/hello
```

## Project Structure

```text
devops-demo
│
├── .github/
│   └── workflows/
│       └── build.yml
│
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
│
├── src/
│
├── Dockerfile
├── pom.xml
└── README.md
```

## Build Locally

Clone the repository:

```bash
git clone git@github.com:YaraL10/DevOps-demo.git
cd DevOps-demo
```

Build the project:

```bash
mvn clean package
```

Run the application:

```bash
mvn spring-boot:run
```

Access:

```text
http://localhost:8080/hello
```

## Docker

Build the image:

```bash
docker build -t devops-demo .
```

Run the container:

```bash
docker run -p 8080:8080 devops-demo
```

## Docker Hub

Pull the published image:

```bash
docker pull yara1110/devops-demo:latest
```

Run it:

```bash
docker run -p 8080:8080 yara1110/devops-demo:latest
```

## Kubernetes

Deploy the application:

```bash
kubectl apply -f k8s/
```

Verify deployment:

```bash
kubectl get deployments
kubectl get pods
kubectl get services
```

Scale the deployment:

```bash
kubectl scale deployment devops-demo --replicas=5
```

## CI/CD Pipeline

GitHub Actions automatically:

- Checks out the source code
- Sets up Java 17
- Builds the application with Maven
- Builds a Docker image
- Pushes the image to Docker Hub

Workflow location:

```text
.github/workflows/build.yml
```

## Docker Image

Docker Hub Repository:

```text
yara1110/devops-demo
```

## Author

**Yara Allama**

- GitHub: https://github.com/YaraL10
- Docker Hub: https://hub.docker.com/u/yara1110