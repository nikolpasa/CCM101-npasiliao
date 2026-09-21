Laboratory 04: Cloud-Native Engineer

Mission Overview

This laboratory activity introduces the fundamental concepts of containerization using Docker within an Ubuntu environment. The mission involves exploring the Docker engine status, deploying an Nginx web server container from Docker Hub, mapping network ports, and executing the complete container lifecycle (starting, stopping, and removing containers).

Objectives

Verify the operational status of the Docker engine and its system service.

Download (pull) and deploy an official Nginx container in detached mode.

Configure port mapping to expose a containerized web service to the local host.

Manage running containers using standard Docker lifecycle commands.

Document the process, commands, and troubleshooting steps used during the deployment.

Docker Commands Executed

Checkpoint 3 (System Status):

sudo systemctl status docker

docker info

Checkpoint 4 (Deploy First Container):

sudo docker pull nginx

sudo docker run -d --name my-nginx -p 8080:80 nginx

curl http://localhost:8080

Checkpoint 5 (Container Lifecycle):

sudo docker ps

sudo docker stop my-nginx

sudo docker ps -a

sudo docker rm my-nginx

Skills Learned

Managing systemd services to verify the health of the Docker daemon.

Deploying and interacting with containerized web servers using Docker CLI.

Understanding network isolation and bridging it using host-to-container port mapping.

Safely navigating the container lifecycle to prevent zombie containers and free up system resources.

Challenges Encountered

Docker Socket Permission Denied: When running docker info initially, I received a permission denied while trying to connect to the docker API at unix:///var/run/docker.sock error. This occurs because the standard user is not in the docker group, which can be bypassed by prepending sudo to the command.

Container Name Conflict: When executing the docker run command, I encountered a Conflict error stating that the name my-nginx was already in use by another container ID. This was resolved by checking the existing containers and managing/removing the old instance before deploying the new one with the same name.
