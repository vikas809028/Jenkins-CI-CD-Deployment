# Jenkins Docker Demo

A simple Flask app to test Jenkins CI/CD with Docker and DockerHub.

## Run locally with Docker Compose
```bash
docker-compose up --build
```

Visit: http://localhost:5000

## Steps for Jenkins
1. Configure DockerHub credentials in Jenkins.
2. Add a Jenkins pipeline with steps:
   - Build Docker image
   - Tag it
   - Push to DockerHub
