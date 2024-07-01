# docker-wordpress-mysql
A simple docker compose to deploy Wordpress with MySQL.

Project structure:
```
.env
.gitignore
├── compose.yaml
└── README.md
```

[_compose.yaml_](compose.yaml)
```
services:
  db:
    # We use a MySQL image which supports both amd64 & arm64 architecture
    #image: mysql:8.0.27

  wordpress:
    image: wordpress:latest
    ports:
      - 8080:80
    restart: always
