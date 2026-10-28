# Mission 8 – Cloud Security Engineer Reflection

During this laboratory activity, I learned how important a host-based firewall is in protecting a cloud server. Even if an attacker manages to bypass the physical network perimeter, the firewall installed on the server can still restrict unauthorized connections. This provides an additional layer of security and helps protect important services and information.

I also understood why managing open network ports is necessary for reducing a server's attack surface. Every unnecessary open port can become a possible entry point for attackers. By allowing only essential services, such as SSH on port 22 and the web application on port 8080, administrators can reduce exposure to potential threats.

In a real enterprise environment, leaving a database port such as MySQL port 3306 publicly accessible can create serious security risks. Attackers may attempt brute-force attacks, exploit vulnerabilities, or gain unauthorized access to sensitive business information. Database connections should therefore be restricted to trusted applications and authorized administrators.

This mission helped me realize that deploying a working application is only one part of managing a cloud server. Security configurations must also be considered because incorrect firewall rules, exposed services, and weak access controls can increase the risk of attacks. I learned that firewall rules must be verified carefully, especially when using Docker, because published container ports may bypass normal UFW filtering.

Looking at my GitHub portfolio, I can see how my knowledge has developed across eight cloud computing missions. My repository now covers different areas, including cloud infrastructure, Docker, storage, deployment, operations, and security. Each laboratory activity has helped me become more familiar with Linux commands, technical documentation, and practical cloud computing concepts. Overall, this mission strengthened my understanding of defense in depth and reminded me that maintaining cloud security requires continuous monitoring, proper configuration, and responsible system administration.
