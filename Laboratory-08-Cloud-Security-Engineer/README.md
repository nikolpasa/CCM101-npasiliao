# Laboratory 08 – Cloud Security Engineer

## Mission Overview
This laboratory focuses on securing an Ubuntu cloud server using the Uncomplicated Firewall (UFW). The mission involves deploying an Nginx web application through Docker, auditing network access, and applying firewall rules to reduce unnecessary exposure.

## Objectives
- Understand the Principle of Least Privilege and attack surface.
- Deploy an Nginx web server using Docker.
- Configure UFW with a default-deny incoming policy.
- Allow SSH and TCP port 8080.
- Verify firewall rules and test the web application.
- Document the security configuration using Markdown.

## Commands Executed
```bash
docker pull nginx:latest
docker run -d --name secure-web-app -p 8080:80 nginx:latest
docker ps
curl http://localhost:8080
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl -I http://localhost:8080
```

## Skills Learned
- Managing Docker containers and web applications.
- Configuring a Linux host-based firewall.
- Applying default-deny security policies.
- Managing network ports and access rules.
- Verifying service availability using curl.
- Maintaining technical documentation in GitHub.

## Evidence
- screenshots/vulnerable-app-running.png
- screenshots/firewall-activated.png
- screenshots/firewall-port-allowed.png

## Security Note
A successful localhost curl test verifies application availability but does not prove that external traffic is filtered. Docker-published ports may bypass normal UFW filtering.
