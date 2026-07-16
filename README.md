# Manga library infrastructure

Configuracion de docker compose para levantar los servicios necesarios para el poryecto Manga Library

Actualmente inlcuye:

- PostgreSQL 17
- Adminer para administracion de base de datos
- RabbitMQ 

## Requisitos

- Docker 29.6.1
- Docker compose v5.2.0

## Variables de entorno

Crear un archivo '.env'.

ejemplo:

- POSTGRES_USER=mangaAdmin
- POSTGRES_PASSWORD=password
- POSTGRES_DB=manga

## Ejecucion

Constuir e iniciar contenedores:

```bash
docker compose up -d 
```

Ver servicios activos:

```bash
docker compose ps
```

Ver logs:
```bash
docker compose logs -f 
```

## Puertos

Docker tomara los puertos por defecto de cada servicio, si es necesario usar un puerto se pueden agregar mediante la opcion:

```docker
ports:
  - "host_port:cont_port"
```