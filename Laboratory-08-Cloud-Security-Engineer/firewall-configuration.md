# Firewall Configuration

## Mission 8: Cloud Security Engineer

### 1. Allow SSH Access
```bash
sudo ufw allow ssh
```
This command allows SSH connections on port 22 so administrators can remotely access the server.

### 2. Configure Default Firewall Policies
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```
These commands block incoming connections by default while allowing outgoing network traffic.

### 3. Enable the Firewall
```bash
sudo ufw enable
```
This command activates UFW using the configured firewall rules.

### 4. Verify Firewall Status
```bash
sudo ufw status verbose
```
This command displays the firewall status and default policies.

### 5. Allow TCP Port 8080
```bash
sudo ufw allow 8080/tcp
```
This rule allows incoming TCP traffic on port 8080 for the Nginx web application.

### 6. Verify Numbered Firewall Rules
```bash
sudo ufw status numbered
```
This command displays the configured firewall rules with their corresponding numbers.

### 7. Test the Web Application
```bash
curl http://localhost:8080
```
This command checks whether the Nginx application responds locally.

### 8. Importance of Allowing SSH Before Enabling UFW
Enabling UFW before allowing SSH could block remote administration and disconnect the administrator from the server.

### Security Note
Docker-published ports may bypass UFW's normal incoming filtering, so additional network-level verification is needed to confirm external access restrictions.
