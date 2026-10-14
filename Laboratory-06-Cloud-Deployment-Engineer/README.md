# Laboratory 6: The Cloud Deployment Engineer

## Mission Overview

This laboratory activity focuses on deploying a multi-tier private cloud storage application using Docker Compose. The deployment uses Nextcloud as the web application and MariaDB as the database. Both services are defined in a YAML configuration file, allowing them to be managed together.

## Objectives

- Explain the concept of two-tier architecture.
- Identify the roles of the web/application tier and database tier.
- Create and understand a `docker-compose.yml` configuration file.
- Deploy and manage multiple containers using Docker Compose.
- Access a web application through a browser using port mapping.
- Document deployment procedures and Infrastructure as Code principles.
- Maintain a structured cloud computing portfolio in GitHub.

## Commands Executed

The following commands are used throughout the mission:

```bash
# Navigate to the deployment directory
cd ~/nextcloud-deployment

# Create and edit the Docker Compose file
nano docker-compose.yml

# Validate the Compose configuration
docker compose config

# Deploy the application in the background
docker compose up -d

# Check the container status
docker compose ps

# View application and database logs
docker compose logs --tail=50 app database

# Stop and remove the containers
docker compose down

# Navigate to the Laboratory 6 documentation
cd ~/CCM101-npasiliao/Laboratory-06-Cloud-Deployment-Engineer
```

## Skills Learned

- Understanding multi-tier application architecture.
- Writing YAML configuration files with correct indentation.
- Deploying Nextcloud and MariaDB using Docker Compose.
- Configuring database connection environment variables.
- Understanding Docker networking and service discovery.
- Using port mapping to access a web application.
- Managing container lifecycles and inspecting logs.
- Applying Infrastructure as Code principles.
- Writing Markdown documentation and maintaining a GitHub portfolio.

## Screenshots

Deployment evidence is stored in the `screenshots/` directory.

- `compose-deployment.png` — successful deployment and running containers.
- `nextcloud-web.png` — Nextcloud installation page in the browser.
- `compose-teardown.png` — container teardown evidence.
