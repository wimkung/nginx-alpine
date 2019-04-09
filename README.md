This project is Dockerfile NGINX v1.15.10 with ALPINE for build and deployment.

## Nginx Dockerfile


This repository contains **Dockerfile** of [Nginx](http://nginx.org/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/wimkung/nginx-alpine/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).


### Base Docker Image

* [_/alpine](https://hub.docker.com/_/alpine)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/wimkung/nginx-alp/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull wimkung/nginx-alpine`

   (alternatively, you can build an image from Dockerfile: `docker build -t="wimkung/nginx-alpine" github.com/wimkung/nginx-alpine`)


### Usage

    docker run -d -p 80:80 wimkung/nginx-alpine

#### Attach persistent/shared directories

    docker run -d -p 80:80 -v <sites-enabled-dir>:/etc/nginx/conf.d -v <certs-dir>:/etc/nginx/certs -v <log-dir>:/var/log/nginx -v <html-dir>:/var/www/html wimkung/nginx-alpine

After few seconds, open `http://<host>` to see the welcome page.
