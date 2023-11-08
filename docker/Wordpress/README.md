# Wordpress docker-compose.yml

> To create a docker container to run Wordpress with MySQL.

## How to use it

- Clone this repository.

```
git clone https://github.com/cdterry87/wordpress-docker-compose-yml mysitename
cd mysitename
```

- Build the docker container. This will take several minutes to create your container and copy all the necessary files over.

```
docker-compose up -d
```

- Once the container has finished building, go to `http://localhost:8000` in your browser and go through the Wordpress installation.

- Start modifying your Wordpress site!
