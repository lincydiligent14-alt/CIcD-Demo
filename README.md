# CI/CD Web Project

This project uses:
- Nginx to serve the static website
- Docker to containerize the app
- Docker Hub to store the image
- GitHub Actions to build and push the image

## Setup
1. Create Docker Hub secrets in GitHub:
   - `DOCKER_USERNAME`
   - `DOCKER_PASSWORD`
2. Push to the `main` branch to trigger the workflow.
3. The image will be published as `YOUR_DOCKER_USERNAME/cicd-web:latest`.
