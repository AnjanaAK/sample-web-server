# sample-web-server

A simple customized web server with apache2 for testing purposes
<br/>

> Find the image [here](https://hub.docker.com/repository/docker/anjana95/sample-web-server) already pushed to docker hub. <br/>
> You can pull it from there and use it locally. Otherwise, you can build your own image with customized index.html page.
<br/>

## Build image

```bash
$ docker build -t sample-web-server:latest .
```

## Run as a container

Run a docker container using the image:

```bash
$ docker run -d --name web -p 8080:80 sample-web-server:latest
```

See the container with name `web` is running now:

```bash
$ docker ps
```

Confirm if it is working fine by visiting the url in browser:
http://localhost:8080/


Also, you can use Curl in command line for the same purpose:
```bash
$ curl -k http://localhost:8080/
```

## Clean-up

Run the following command to destroy the `web` container:
```bash
$ docker rm -f web
```

## Author

Anjana AK ([@AnjanaAK](https://github.com/AnjanaAK))

