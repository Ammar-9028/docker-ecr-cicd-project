# CloudLaunch — Docker + AWS ECR + EC2

A beginner-friendly static website project for learning container-based deployment.

## Files
- `index.html` — website content
- `style.css` — website design
- `Dockerfile` — packages the site into an Nginx Docker image

## Run locally with Docker

```bash
docker build -t cloudlaunch .
docker run -d --name cloudlaunch -p 8080:80 cloudlaunch
```

Open: http://localhost:8080

Stop and remove:

```bash
docker rm -f cloudlaunch
```

## Deployment flow

GitHub → GitHub Actions → Docker image → Amazon ECR → EC2

The GitHub Actions workflow will be added in the next setup step after AWS and GitHub settings are ready.
