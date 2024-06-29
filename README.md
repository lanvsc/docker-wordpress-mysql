# docker-wordpress-mysql
#A simple docker compose to deploy Wordpress with MySQL.

PROJECT STRUCTURE:
.
.gitignore
.env
├── compose.yaml
└── README.md

COMPOSE.YAML

services:
  db:
    # We use a NySQL image which supports both amd64 & arm64 architecture
    image: mysql:5.7
    ...
  wordpress:
    image: wordpress:latest
    ports:
      - 8080:80
    restart: unless-stopped
    ...