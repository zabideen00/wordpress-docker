# Setup Instructions

## Create .env file

First create a `.env` file in the root of the project and pass following environment variables

```MARIADB_PASSWORD=secret-password```

```MARIADB_USER=wordpress```

```MARIADB_DATABASE=wordpress```

```MARIADB_ROOT_PASSWORD=super-secret-password```
 
 ## Start wordpress docker
After setting up the environment variables, now start the dockerized wordpress site by running following commadn.

```docker-compose up -d```

The docker compose will start 3 containers

* wordpress [http://localhost:3000](http://localhost:3000)
* mariadb
* phpmyadmin [http://localhost:4000](http://localhost:4000)

You can access wordpress and phpmyadmin by visiting the given URLs. MariaDB runs in the internal docker network so it can not be directly accessed oh host but you can access it via `phpmyadmin`.

Use the credentials passed in the `.env` file to log into the `phpmyadmin`.
