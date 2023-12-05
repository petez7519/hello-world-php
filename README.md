# hello-world-php
Dockerized Hello World App using PHP built in server. Very lightweight because utilizing Linux Alpine image

## Usage

### 1. Directly Pull the Docker Image from the Docker Hub

You can simply pull & run the hello world app image from the Docker Hub

```
docker run -d --name hello-world-php-c1 -p 81:80 areesmoon/hello-world-php
```

Access the app through your browser at http://localhost:81

### 2. Custom Build
Download the github repo and then build the docker image by yourself.

```
git clone https://github.com/areesmoon/hello-world-php.git
```

You can can change file inside the src folder with your own PHP files and the build the image

```
docker build -t areesmoon/hello-world-php .
```

Once finish, run the docker image into container. Note that the default port is 80 for the web service, here forward to port 81 localhost

```
docker run -d --name hello-world-php-c1 -p 81:80 areesmoon/hello-world-php
```

Access the app through your browser at http://localhost:81