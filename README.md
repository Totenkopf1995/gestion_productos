# README

### Proyecto 1: Microservicio de Gestión de Tareas

Este microservicio permite a los usuarios crear, eliminar y modificar tareas. Cuando se realiza un cambio en las tareas, el servicio envía una notificación al segundo microservicio, que se encarga de notificar al usuario por correo electrónico.

#### Características
- Crear tareas
- Eliminar tareas
- Modificar tareas
- Envío de notificaciones a través de un segundo microservicio

#### Requisitos
- Ruby 3.0 o superior
- Rails 6.0 o superior
- Base de datos (PostgreSQL, MySQL, etc.)
- Redis (opcional, para gestión de colas)

#### Instalación
1. Clonar el repositorio:
   ```bash
   git clone https://github.com/Totenkopf1995/gestion_productos.git
   cd microservicio-tareas
2. Instalar las gemas necesarias:
   ```bash
   bundle install
3. Configurar la base de datos:
    
   Edita el archivo config/database.yml con tus credenciales.
    
   Luego, ejecuta:
   ```bash
   rails db:create
   rails db:migrate
4. Configurar el entorno:
   Asegúrate de tener configuradas las variables de entorno necesarias, como la URL del segundo microservicio.

5. Iniciar el servidor:
   ```bash
   rails server

#### Uso
- Crear una tarea:

  Realiza una solicitud POST a /tasks con los parámetros necesarios.
- Eliminar una tarea:

  Realiza una solicitud DELETE a /tasks/:id.
- Modificar una tarea:

  Realiza una solicitud PATCH a /tasks/:id con los nuevos datos.