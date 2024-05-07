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

![Despliegue](images/Despliegue_DockerCompose.jpeg)

- Despligue con este repositorio

  `git clone https://github.com/delmylira48/LMS-Moodle.git`

  `cd LMS-Moodle`

  `docker compose up`

## Configuración de Moodle

### Paso 1) Ingresar al Moodle
 
Ingresamos en el navegador con `localhost` en el puerto `80`. Esto cargará la pagina principal de Moodle.
- http://localhost:80
- Damos click en `Log in`

![home](images/Home.jpeg)

### Paso 2) Login Moodle
Capturar las credenciales y dar click en `Log in`
- User: User
- Password: bitnami

![login](images/Login.jpeg)

Una vez dentro, verás este panel de administador

![PanelAdmin](images/Panel_Admin.jpeg) 

### Paso 3) Crear nuevo usuario
Crear los usuarios necesarios:
- Click en `Site administration`
- Click en `Users`
- Click en `Add a new user`

A continuación llenar todos los campos requeridos y guardamos.

![NewUser](images/Add_New_User.jpeg)

### Paso 4) Crear nuevo curso
- Click en `Site administration`
- Click en `Courses`

![Panel](images/SiteAdmin-Courses.jpeg)

- Click en `Add a new course`

A continuación llenar todos los campos requeridos y guardamos.

![NewCourse](images/New_Course.jpeg)

![PanelCourse](images/Panel_Curso1.jpeg)

Para el siguiente paso dar click en `Participants`
### Paso 5) Agregar a los participantes al curso
- Click en `Enrol users`
- Buscar los participantes existentes y agregarlos

![AddParticipants](images/Add_Users_To_Course.jpeg)

### Paso 6) Asignar roles a los participantes del curso
- Click en `Participants`

![ParticipantsCourse](images/Course_Participants.jpeg)
- Click en el icono de lapiz en la columna `Roles`
- Seleccionar todos los para asignar a cada participante

![AddRoles](images/Assign_Roles.jpeg)

- Click en el icono de Guardar

![AllParticipants](images/All_Participants_Courses_With_Roles.jpeg)

