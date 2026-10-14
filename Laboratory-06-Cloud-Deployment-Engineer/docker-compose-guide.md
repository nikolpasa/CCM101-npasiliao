# Docker Compose Guide

## 1. What Does the `services:` Block Do?

The `services:` block defines the containers that make up an application in a Docker Compose configuration file. In this mission, it defines two services: `database` and `app`. The `database` service uses the MariaDB 10.6 image, while the `app` service uses the Nextcloud image. Docker Compose uses these definitions to create and manage the containers together.

## 2. How Does Nextcloud Find the Database Container?

Nextcloud finds the database through the `MYSQL_HOST` environment variable, which is set to `database`. This value matches the service name of the MariaDB container in the Compose file. Docker Compose provides network-based service discovery, allowing the Nextcloud container to connect to MariaDB using that service name instead of requiring a manually assigned IP address.

Other environment variables configure the database connection:

- `MYSQL_DATABASE` specifies the database name.
- `MYSQL_USER` specifies the database username.
- `MYSQL_PASSWORD` specifies the database user's password.
- `MYSQL_HOST` specifies the database service hostname.

These settings allow Nextcloud to connect to the database with the appropriate configuration.

## 3. Difference Between `docker run` and `docker compose up -d`

The `docker run` command starts an individual container using the options provided in the command. When deploying several related containers manually, an engineer must configure and start each container separately.

The `docker compose up -d` command reads the `docker-compose.yml` configuration file and creates or starts the services defined in it. The `-d` option runs the containers in the background, allowing the terminal to be used for other tasks. This approach makes multi-container deployments easier to repeat, manage, and maintain.

## 4. Infrastructure as Code (IaC)

Infrastructure as Code is the practice of defining and managing infrastructure through configuration files instead of relying only on manual commands. The `docker-compose.yml` file describes the services, images, environment variables, ports, and other configuration required by the application.

Using Docker Compose helps make deployments consistent and easier to reproduce. Engineers can review, document, and version-control configuration files, making infrastructure management more organized.

## 5. Conclusion

Docker Compose simplifies the deployment of multi-tier applications by allowing related containers to be defined in one configuration file. In this mission, Nextcloud provides the web application while MariaDB manages the database. Understanding their relationship helps cloud engineers deploy and maintain containerized applications more efficiently.
