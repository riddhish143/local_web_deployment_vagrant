# Prerequisites
- JDK 11 
- Maven 3 
- MySQL 8

# Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- Tomcat
- MySQL
- Memcached
- Rabbitmq
- ElasticSearch

# Database
Here,we used Mysql DB 
sql dump file:
- /src/main/resources/db_backup.sql
- db_backup.sql file is a mysql dump file.we have to import this dump to mysql db server
- mysql -u <user_name> -p accounts < db_backup.sql


# Web Application Deployment with Vagrant and Linux

This project demonstrates the deployment of a web application using Vagrant and Linux. The application stack includes Nginx as the web server, Tomcat as the application server, RabbitMQ for messaging, and Memcache for caching.

## Prerequisites

- Vagrant
- VirtualBox or another Vagrant-supported provider
- Git (optional, for cloning this repository)

## Getting Started

1. **Clone the Repository (optional):**
   ```sh
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```

2. **Start the Vagrant Environment:**
   ```sh
   vagrant up
   ```

3. **Access the Web Application:**
   Once the setup is complete, you can access the web application via your web browser at `http://localhost:8080`.

## Components

- **Nginx:** Acts as a reverse proxy to handle incoming HTTP requests.
- **Tomcat:** Serves as the application server where the web application is deployed.
- **RabbitMQ:** Manages the messaging queues for the application.
- **Memcache:** Provides caching to enhance performance.

## Configuration

The provisioning scripts and configurations are located in the `Vagrantfile` and associated shell scripts. These files handle the installation and setup of all components.

## Notes

- Ensure that ports `8080`, `80`, and any other required ports are open and not in use by other applications.
- Customize configurations as needed in the `Vagrantfile` and shell scripts to suit your specific requirements.

## Troubleshooting

- If the VM fails to start, try running `vagrant destroy` followed by `vagrant up` to reset the environment.
- Check the logs for Nginx, Tomcat, RabbitMQ, and Memcache located in `/var/log/` on the VM for any errors.
