List running containers

sudo docker ps


Explanation: This command lists all active, currently running Docker containers on the system along with their container IDs, image names, and port mappings.

Stop the running container

sudo docker stop my-nginx


Explanation: This command gracefully halts the running execution of the container named "my-nginx" without deleting its data.

Verify it is stopped

sudo docker ps -a


Explanation: This command displays all containers (both running and stopped), allowing us to confirm that "my-nginx" is now listed with an "Exited" status.

Remove the container completely

sudo docker rm my-nginx


Explanation: This command permanently deletes the stopped container instance and its associated writable layer from the local system.
