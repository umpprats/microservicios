# PostgreSQL
## Requisitos previos
1. Tener instalado **docker**
    - Para **windows** https://docs.docker.com/desktop/setup/install/windows-install/
    - Para **linux** https://docs.docker.com/desktop/setup/install/linux/ (Siempre instalar desde los repositorios oficiales de docker)
2. Desde consola / terminal:
```
# Servidor de PostgreSQL
docker pull postgres:15.4-bullseye
# Cliente Web para PostgreSQL
docker pull docker pull dpage/pgadmin4:9.2
```
3. Crear una red en docker

`docker network create mired`
## Estructura para la carpeta PostgreSQL
```
carpeta_del_usuario
├── postgresql
│   └── data # Carpeta donde se crearan las bases de datos
│   └── docker-compose.yml
│   └── .env # Renombrar .env-example y cambiar los valores de las variables de entorno
├── pgadmin
│   └── docker-compose.yml
│   └── .env # Renombrar .env-example y cambiar los valores de las variables de entorno
```
## Ejecución de PostgreSQL
```
# en cada carpeta (pgadmin y postgresql) ejecutar:
docker compose up
```
# Utilidades Varias
1. Descargar mkcert https://github.com/FiloSottile/mkcert/tags

## Instalar
```
mkcert -cert-file certs/cert.pem -key-file certs/key.pem "universidad.localhost" "*.universidad.localhost" 127.0.0.1 ::1
mkcert -install
```

