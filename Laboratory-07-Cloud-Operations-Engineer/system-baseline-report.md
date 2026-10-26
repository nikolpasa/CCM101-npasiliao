# System Baseline Report

## Mission 7: The Cloud Operations Engineer

### 1. Memory (RAM) Monitoring

**Command Executed:**
`free -h`

- Total RAM: [Enter actual value]
- Used RAM: [Enter actual value]
- Available RAM: [Enter actual value]

**Observation:**

The `free -h` command displayed the server's memory usage. This helped me understand how much RAM was being used and how much remained available for running applications.

### 2. Disk Storage Monitoring

**Command Executed:**
`df -h /`

- Total Storage Capacity: [Enter actual value]
- Used Storage: [Enter actual value]
- Available Storage: [Enter actual value]
- Disk Usage: [Enter actual percentage]

**Observation:**

Checking disk space is important before a massive traffic surge because insufficient storage could prevent the server from saving logs and application data, potentially causing errors or service interruptions.

### 3. CPU and Process Monitoring

**Command Executed:**
`top`

**Observation:**

The `top` command displayed real-time CPU usage, memory consumption, and active processes. This helped me observe the server's current workload and identify processes that might consume too many resources.

### 4. Conclusion

By using Linux monitoring commands, I learned how to check the basic health of a server before deploying and monitoring a web application. These checks are important for identifying potential resource limitations.

### 5. Screenshot Evidence

- [Memory Check](screenshots/memory-check.png)
- [Disk Check](screenshots/disk-check.png)
