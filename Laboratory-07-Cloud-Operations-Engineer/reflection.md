# Mission 7 Reflection – The Cloud Operations Engineer

### 1. Why is it important to check the host server's resources even if your containers are running perfectly?

It is important to check the host server's resources because containers still depend on the server's CPU, memory, and storage. Even if the containers are working properly, the server may experience problems when its resources become limited. By using commands such as `free -h`, `df -h`, and `top`, I can monitor the server's condition and identify possible problems before they affect the applications.

### 2. If a user complains that they cannot log into a web application, how would the docker logs command help you solve the problem?

The `docker logs` command helps me identify errors and activities happening inside a container. If a user cannot log in, I can examine the logs to look for failed requests, error messages, or other possible issues. This helps me understand where the problem might be coming from instead of guessing.

### 3. What is the difference between monitoring logs and monitoring metrics?

Logs provide detailed records of events and errors that happen inside an application. Metrics show numerical information such as CPU usage, memory consumption, and network activity. Logs help explain what happened, while metrics help show how the application is performing.

### 4. How do large enterprise companies monitor thousands of containers at the same time?

Large companies use monitoring tools such as Prometheus and Grafana to monitor many containers. Prometheus collects performance metrics, while Grafana displays the information through dashboards. These tools help engineers monitor their systems and identify performance problems more efficiently.

### 5. How has your ability to troubleshoot Linux environments improved?

My troubleshooting skills have improved because I am becoming more familiar with Linux commands and Docker tools. I learned how to check system resources, examine application logs, and monitor container performance. This activity helped me become more confident in using the Linux terminal and understanding how cloud applications are monitored.
