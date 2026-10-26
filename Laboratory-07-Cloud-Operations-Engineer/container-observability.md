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
