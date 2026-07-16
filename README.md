# Manga library infrastructure

Configuracion de docker compose para levantar los servicios necesarios para el poryecto Manga Library

Actualmente inlcuye:

- PostgreSQL 17
- Adminer para administracion de base de datos

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