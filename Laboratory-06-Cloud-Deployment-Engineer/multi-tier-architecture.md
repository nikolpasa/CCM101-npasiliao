# Multi-Tier Architecture

## What Is a Two-Tier Architecture?

A two-tier architecture is an application design that separates an application into two main parts: the Web/Application Tier and the Database Tier. These tiers communicate with each other to provide services to users. In this mission, we will use Nextcloud as the application and MariaDB as the database.

## 1. The Web/Application Tier

The Web/Application Tier is responsible for displaying the user interface and handling requests from users. It receives HTTP requests through a web browser and processes the actions users perform in the application.

In this deployment, **Nextcloud** serves as the Web/Application Tier. It provides the interface that allows users to access and manage their files through a web browser. It also communicates with the database to retrieve or store information needed by the application.

## 2. The Database Tier

The Database Tier stores and manages persistent application data, such as user accounts, credentials, and file metadata. It allows the application to retrieve and update information when needed.

In this mission, **MariaDB** serves as the Database Tier. It stores information used by Nextcloud and communicates with the application container so that the system can function properly.

## 3. Why Separate the Tiers?

Separating the web application and database into two containers makes the system easier to manage, troubleshoot, and maintain. Each container has its own responsibility, allowing engineers to update or restart one component without necessarily rebuilding the other. This separation also makes it easier to scale the application and configure access between services.
