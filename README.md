# Despliegue y configuración de LMS Moodle con Docker Compose

## Usuarios y contraseñas 
### MariaDB 
- MOODLE_DATABASE_USER=bn_moodle
- ALLOW_EMPTY_PASSWORD=yes

**Se recomienda configurar una contraseña modificando el archivo docker-compose.yml**
- MOODLE_DATABASE_PASSWORD= <<CONTRASEÑA>>
- ALLOW_EMPTY_PASSWORD=no
### Moodle 

**Credenciales para ingresar como administrador**
- USER=user
- PASSWORD=bitnami

## Despliegue con Docker Compose 

- Despliegue con docker compose siguiendo la documentación [bitnami/moodle](https://hub.docker.com/r/bitnami/moodle/#!)

  `curl -sSL https://raw.githubusercontent.com/bitnami/containers/main/bitnami/moodle/docker-compose.yml > docker-compose.yml
docker-compose up -d`

- Despligue con este repositorio

  `git clone https://github.com/delmylira48/LMS-Moodle.git`

  `cd LMS-Moodle`

  `docker compose up`

## Configuración de Moodle
