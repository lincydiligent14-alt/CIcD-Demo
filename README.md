# CI/CD Web Project

This project uses:
- Nginx to serve the static website
- Docker to containerize the app
- Docker Hub to store the image
- GitHub Actions to build and push the image

## Setup
1. Create a Docker Hub repository, for example `cicd-web`.
2. Add these GitHub repository secrets:
   - `DOCKER_USERNAME`
   - `DOCKER_PASSWORD`
3. Push to the `main` branch to trigger the workflow.
4. The image will be published as `YOUR_DOCKER_USERNAME/cicd-web:latest`.

## Run locally
```bash
docker compose up --build
```
Then open http://localhost:8080

## Deploy to a server
Add these GitHub secrets before enabling deployment:
- `DOCKER_USERNAME`
- `DOCKER_PASSWORD`
- `DEPLOY_HOST`
- `DEPLOY_USERNAME`
- `DEPLOY_SSH_KEY`
- `DEPLOY_PORT` (optional, default is 22)

The server must have Docker installed and accessible over SSH.
