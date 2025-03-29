## Requirements

- [NodeJS](https://nodejs.org/en)
- [PNPM](https://nodejs.org/en)
- [NestJS](https://nestjs.com/)
- [Docker](https://www.docker.com/)

## Extensiones Recomendadas
- Prisma
- Prisma UML
- Database Client
- Dotenv
- NestJS File Generator
- Node.js Modules Intellisense
- TODO Highlight

## Instalación de recursos
<details>
<summary>Arch Linux</summary>
<br>

**Node.js**

```bash
$ yay -S nodejs
```

**NPM**

```bash
$ yay -S npm
```

**PNPM**

```bash
$ npm install -g pnpm
```

**NestJS**

```bash
$ pnpm add -g @nestjs/cli
```


**Docker**

```bash
$ yay -S docker
```


**Docker Compose**

```bash
$ yay -S docker-compose
```
</details> 


<details>
<summary>Ubuntu</summary>
<br>

**Node.js**

**Actualizar los paquetes del sistema**

```bash
$ sudo apt update && sudo apt upgrade -y
```

**Instala curl y ca-certificates**

```bash
$ sudo apt install curl ca-certificates -y
```

**Descarga e instala el repositorio de NodeSource:**

```bash
$ curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
```

**Instala Node.js y npm:**

```bash
$ sudo apt install nodejs -y
```

**Docker y docker compose**

```bash
$ sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y

```

</details> 


<details>
<summary>Windows</summary>
<br>

**Node.js**

- [NodeJS](https://nodejs.org/en)

![Imagen de WhatsApp 2025-03-25 a las 04 16 10_6f69a56b](https://github.com/user-attachments/assets/92e98aba-6390-4c7a-b802-35e9012db450)

- [Docker](https://www.docker.com/)

![Imagen de WhatsApp 2025-03-25 a las 04 17 37_1af1c76d](https://github.com/user-attachments/assets/ae9ea941-a5e4-4b9b-9893-61d0b73a4e8c)


</details> 

## Clonar Repositorio

```bash
$ git clone https://github.com/Uguimar-Platform/launcher.git
```

## Actualizar Submódulos de git
Ubicarse en la carpeta raíz del Launcher.
```bash
$ git submodule update --init --recursive
```

## Cambiar de rama
Cambiar de rama de los submódulos si es necesario.
Ubicarse en la carpeta raíz de cada microservicio.

```bash
$ git checkout develop
```


## Instalar Dependencias
Ubicarse en la carpeta raíz de cada microservicio y ejecutar
```bash
$ pnpm i
```

## Crear los archivos .env en Client Gateway y Auth Microservice

## Client Gateway (API Gateway)
```bash
PORT=3000
NATS_SERVERS="nats://localhost:4222"
SWAGGER_USERNAME=admin
SWAGGER_PASSWORD=admin
ENV=local
```

## Auth-ms
```bash
DATABASE_URL="postgresql://postgres:postgres@localhost:5432/authdb-ms"
PORT=3001
NATS_SERVERS=nats://nats-server:4222
JWT_SECRET=05ac0f5e874b124a0ebbfa80a4e3f7956f5e1dc3beddbcff1135ca9fe0b2dfc02bc6248f33d19c0b8d85903d2306f40c1b5b11955f64a0da75c4d72e94e7595c
```

## Ejecutar Docker
Solo si es la primera vez que ejecutarás el proyecto.
Ubicarse en la carpeta raíz de Launcher y ejecutar:
```bash
$ docker compose up
```
 
Si NO es la primera vez que ejecutarás el proyecto.
Ubicarse en la carpeta raíz de Launcher y ejecutar:
```bash
$ docker compose up --build
```

## Ejecutar prisma

```bash
$ pnpx prisma generate
```


## Ejecutar migraciones de prisma
Ejecutar este comando cuando la aplicación ya ha sido dockerizada.
```bash
$ pnpx prisma migrate dev
```

## Abrir el Swagger del Microservicio de Autenticación

```bash
$ http://localhost:3000/docs/auth
```

> [!NOTE]  
> El puerto es el especificado anteriormente en la puerta de enlace del cliente en el entorno
