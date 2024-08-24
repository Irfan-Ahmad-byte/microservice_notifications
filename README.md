# Notifications Microservice

This is a sample microservice, built with FastAPI/Python. This service can b run in 2 ways:

1- building the image manually

2- through docker compose


## Build image and run manually

1- `docker network create --driver bridge microservice-net`

2- `docker run -d --name postgresql-server --network microservice-net -e POSTGRESQL_PASSWORD=mysupersecretpassword bitnami/postgresql`

3- `docker build -t notifications-microservice .`

4- `docker network connect microservice-net notifications-microservice`

5- `docker run -p 8000:8000 notifications-microservice`


## Run through Docker Compose

`docker compose up` or `docker compose up -d`