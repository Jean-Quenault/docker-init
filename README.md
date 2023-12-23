# Docker Compose for PHPMyAdmin and MySQL

This project sets up a dockerized environment with PHPMyAdmin and MySQL using Docker Compose.

## Prerequisites

- Docker installed on your machine.
- Docker Compose installed on your machine.

## Installation and Startup

1. **Clone the repository** (if you have placed the `docker-compose.yml` file in a git repository) or simply **place the `docker-compose.yml` file in a folder** on your machine.
2. **Navigate to the folder** containing the `docker-compose.yml` file.
3. **Start the services** with the following command:
   `docker-compose up -d`
   This command will download the necessary images and start the containers in the background.

## Accessing PHPMyAdmin

Open your browser and go to [http://localhost:8080](http://localhost:8080). Use the following credentials to log in:
- **User**: `root`
- **Password**: `example` (replace it with the password you have set in the `docker-compose.yml` file).

## File Structure

- `db`: Service for the MySQL server.
- `phpmyadmin`: Service for the PHPMyAdmin web interface.
- `volumes`: A volume named `dbdata` is created for MySQL data persistence.

## Best Practices

- Use of volumes for data persistence.
- Configuration via environment variables.
- Separation of services into distinct containers.
- Automatic restart of services.

## Security

- **Change the root password** in the `docker-compose.yml` file to secure your database.
- Do not share your `docker-compose.yml` file containing passwords or keys.

## References

For more information, please consult the following resources:
- [Docker Volumes Documentation](https://docs.docker.com/storage/volumes/)
- [Configuring Docker and Docker Compose on AWS EC2 (Amazon Linux 2023 AMI)](https://medium.com/@fredmanre/how-to-configure-docker-docker-compose-in-aws-ec2-amazon-linux-2023-ami-ab4d10b2bcdc)
