# Laboratory Activity 7 – The Cloud Operations Engineer

## Mission Overview

In this laboratory activity, I acted as a Cloud Operations Engineer at CloudNova Technologies. My task was to monitor the health and performance of a Linux server and a containerized Nginx web application using the KillerCoda Ubuntu Playground.

I used Linux commands to check the server's memory, disk storage, and CPU activity. I also deployed an Nginx container using Docker, simulated website traffic, and examined application logs and container performance metrics.

This activity helped me understand the importance of monitoring and observability in maintaining reliable cloud applications.

## Objectives

The objectives of this laboratory activity were to:

1. Monitor Linux server resources, including RAM, CPU, and disk storage.
2. Deploy an Nginx web server using Docker.
3. Simulate successful and unsuccessful HTTP requests.
4. Retrieve and analyze Docker application logs.
5. Monitor real-time container CPU and memory usage.
6. Document system performance and monitoring results using Markdown.
7. Maintain an organized GitHub Cloud Computing Portfolio.

## Monitoring Commands Executed

| Command | Purpose |
|---|---|
| `free -h` | Display the server's memory usage and available RAM. |
| `df -h /` | Check the disk capacity and available storage of the root filesystem. |
| `top` | Monitor CPU usage, memory, and running processes. |
| `docker ps` | Display running Docker containers. |
| `docker run -d --name client-website -p 8080:80 nginx` | Deploy an Nginx web server container. |
| `curl http://localhost:8080/` | Generate a successful HTTP request. |
| `curl http://localhost:8080/hidden-admin-page` | Generate an HTTP 404 error. |
| `docker logs client-website` | Retrieve Nginx application logs. |
| `docker stats` | Monitor real-time container resource usage. |
| `docker stats client-website --no-stream` | Display a single snapshot of container metrics. |

## Skills Learned

Through this laboratory activity, I developed the following skills:

- **Linux System Monitoring:** I learned how to check server memory, disk storage, CPU usage, and running processes using Linux commands.
- **Docker Container Management:** I practiced deploying and managing an Nginx web server container.
- **HTTP Traffic Simulation:** I learned how to use the `curl` command to generate successful requests and intentionally trigger HTTP errors.
- **Application Log Analysis:** I learned how Docker logs can help identify HTTP requests and troubleshoot application problems.
- **Container Performance Monitoring:** I practiced using Docker metrics to observe CPU usage, memory consumption, and network activity.
- **Technical Documentation:** I improved my ability to organize monitoring results and technical explanations using Markdown.
- **GitHub Portfolio Management:** I practiced maintaining a structured repository and documenting laboratory activities.

## System Baseline Summary

The following results were recorded from the KillerCoda Ubuntu server:

| Resource | Recorded Value |
|---|---|
| Total RAM | 1.9 GiB |
| Used RAM | 464 MiB |
| Available RAM | 1.4 GiB |
| Total Disk Storage | 19 GB |
| Used Disk Storage | 5.5 GB |
| Available Disk Storage | 13 GB |
| Disk Usage | 30% |

## Laboratory Documentation

- [System Baseline Report](system-baseline-report.md)
- [Container Observability Report](container-observability.md)
- [Mission Reflection](reflection.md)
- [Screenshot Evidence](screenshots/)

## Conclusion

This laboratory activity helped me understand how Cloud Operations Engineers monitor servers and containerized applications. I learned that deploying an application is not enough because engineers must also monitor its performance, examine logs, and identify possible problems.

Using Linux and Docker monitoring tools helped me become more familiar with basic cloud operations and troubleshooting.
