# Container Observability Report

## Mission 7: The Cloud Operations Engineer

### Checkpoint 4 – Application Logging

**Command Executed:**

`docker logs client-website`

### 1. Application Log Analysis

I used the `docker logs` command to retrieve the Nginx web server's application logs.

The logs were used to examine the HTTP requests generated during the traffic simulation.

**Successful Requests:**

- HTTP 200 – First successful website visit
- HTTP 200 – Second successful website visit
- HTTP 200 – Third successful website visit

**Failed Request:**

- HTTP 404 – Requested page not found

### 2. HTTP 404 Error Log

**Actual Log Entry:**

```text
[Paste your actual HTTP 404 log line here]
```

### 3. Importance of Application Logs

Application logs are important for troubleshooting because they record requests, errors, and activities that occur within an application. They help cloud operations engineers identify the cause of problems and determine which parts of the application need attention.
## Checkpoint 5 – Real-Time Container Metrics

### 1. Container Resource Monitoring

**Command Executed:**

`docker stats`

I used the `docker stats` command to monitor the real-time performance of the Nginx web server container named `client-website`.

### 2. Container Performance Results

| Metric | Recorded Value |
|---|---|
| Container Name | client-website |
| CPU Usage | [Enter actual CPU %] |
| Memory Usage | [Enter actual MiB] |
| Memory Limit | [Enter actual value] |
| Memory Percentage | [Enter actual %] |
| Network I/O | [Enter actual values] |

### 3. Observation

The `docker stats` command displayed the CPU and memory resources consumed by the Nginx container. By examining these metrics, I was able to observe the container's resource consumption and understand how Docker helps monitor application performance.

### 4. Importance of Container Monitoring

Monitoring container resources is important because it helps cloud operations engineers identify high CPU usage, excessive memory consumption, and possible performance issues.

By regularly checking these metrics, engineers can detect potential resource problems before they affect application availability.

### 5. Screenshot Evidence

[Container Metrics Screenshot](screenshots/container-metrics.png)
