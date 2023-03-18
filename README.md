# WordPress Docker 🐳

<p align="center">
</p>
A generic docker environment for WordPress with mySql


## Insstallation

1. Click [Use this template](https://github.com/rakibdevs/wprdpress-docker/generate)
2. Clone the repository containing the `docker-compose.yml` file.
3. Run the following command to build the Docker image:

```bash
$ docker compose build
```
This command will download all the necessary dependencies and build the Docker image according to the specifications in the Dockerfile.

4. Once the build is complete, run the following command to start the Docker container: 
```bas
$ docker-compose up -d
```

## Acces Webpage
To access the web page for your Laravel project, please follow these steps:

Ensure that the Docker container is running by running the command `docker ps` in your terminal or command prompt. This command will display a list of all the running Docker containers on your system.

Open a web browser and navigate to the following URL: http://localhost:8990. This URL corresponds to the port that has been exposed in the `docker-compose.yml` file for the Nginx service.

## How to setup different WordPress version?
To update the WordPress version for your Docker container, please follow these steps:

Open the `Dockerfile` for your PHP image, which is located in the `docker/wordpress/` directory.

Update the FROM statement to use the base image for the WordPress version you want to use. For example, to use WordPress version 6.1.1, you can change the FROM statement to the following:

```bash
FROM 6.1.1-apache
```
Find the available wordpress official docker images [here](https://hub.docker.com/_/wordpress)
Save the Dockerfile and build the Docker image again using the `docker-compose build` command.

Once the build is complete, start the Docker container using the `docker-compose up` command.
