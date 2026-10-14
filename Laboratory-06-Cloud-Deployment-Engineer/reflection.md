# Mission 6: The Cloud Deployment Engineer — Reflection

This laboratory activity helped me understand how Docker Compose makes deploying cloud applications easier and more organized. Instead of manually creating and configuring each container, I learned that I can define the services in a single `docker-compose.yml` file. This makes deployment faster, more consistent, and easier to repeat. It also helps cloud engineers manage related services using only a few commands.

I also learned that YAML indentation is very important. YAML uses spaces to organize configuration settings and show which properties belong to each service. If I use incorrect indentation or a Tab instead of spaces, Docker Compose may report a syntax error or interpret the configuration incorrectly. This taught me to be careful when writing configuration files and to validate them before deploying an application.

Environment variables such as `MYSQL_DATABASE`, `MYSQL_USER`, and `MYSQL_PASSWORD` allow the application and database to use matching connection settings. The `MYSQL_HOST` variable tells Nextcloud where to find the MariaDB service. I now understand how these settings help connect two separate containers. However, sensitive credentials should be managed more securely in real production environments.

Deploying a private cloud storage application such as Nextcloud was an interesting experience because it showed me how several components can work together in a short time. Instead of setting up every service separately, Docker Compose allowed me to describe the infrastructure in one file. This helped me appreciate the value of automation and proper configuration.

Since Mission 1, my understanding of cloud computing has grown from learning basic Linux commands and exploring the cloud environment to managing containerized applications and multi-tier architecture. I have learned that cloud engineering involves more than starting servers. It also requires planning, configuration, documentation, testing, and troubleshooting. This mission improved my confidence in using Docker and showed me how Infrastructure as Code can help engineers deploy applications efficiently and consistently.
