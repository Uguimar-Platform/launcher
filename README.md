## Description

Launcher for all microservices and client-gateway

## Project setup

```bash
$ git submodule update --init --recursive
```


## Install dependencies

```bash
$ pnpm i
```

## Create the environment variable files in client, gateway, and auth microservices

## Auth Microservice
```bash
PORT=
DATABASE_URL=
NATS_SERVERS=
```

## Client Gateway
```bash
PORT=
NATS_SERVERS=
```


## Docker setup

```bash
$ docker compose up
```


## Open Swagger Microservice Authentication

```bash
$ http://localhost:3000/docs/auth
```

> [!NOTE]  
> The port is as specified above in your client gateway in the env
