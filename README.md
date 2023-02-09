# A docker compose for Authelia with external nginx reverse proxy

## Dependencies

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose plugin](https://docs.docker.com/compose/install/linux/)

## Please see the [documentation](https://www.authelia.com/integration/deployment/docker/#lite) and [nginx examples](https://www.authelia.com/integration/proxies/nginx/#standard-example) for usage instructions

## Generate hashed password for users in portal/config/users_database.yml

```bash
docker run --rm authelia/authelia:latest authelia hash-password 'your_secret_value'
```

## Installation

```bash
git clone https://github.com/unleftie/authelia-compose.git
cd authelia-compose
cp .env.example .env # don't forget to change default values
chmod 600 .env
docker compose up -d
```

## Uses the following Docker containers

- https://hub.docker.com/r/authelia/authelia
- https://hub.docker.com/_/redis

## 📝 License

This project is licensed under the [MIT](LICENSE).
