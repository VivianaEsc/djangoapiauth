```markdown
# Proyecto API Rest con Django y Django Rest Framework

## Descripción del Proyecto
Este proyecto implementa una API Rest utilizando Django y la librería Django Rest Framework (DRF). Contiene configuraciones para la conexión a una base de datos MySQL y un módulo para la gestión de usuarios con funcionalidades de creación, login, logout y autenticación mediante JSON Web Token (JWT).

## Contenidos
1. [Conexión a base de datos MySQL] 
2. [Módulo para gestión de usuarios] 
   - [Método para creación de usuario] 
   - [Método para Login] 
   - [Método para Logout] 
   - [Método para utilización de JSON Web Token en autenticación](#24-método-para-utilización-de-json-web-token-en-autenticación)
   - [Modelo de datos] 
### 1. Conexión a base de datos MySQL
#### Herramientas
- Django
- MySQL
- Conector MySQL para Python (por ejemplo, MySQLclient)

#### Proceso
1. **Instalar el conector MySQL**: Instala el conector necesario para que Django pueda comunicarse con MySQL.
2. **Configurar la conexión en Django**: Modifica el archivo de configuración de Django (`settings.py`) para incluir los detalles de la base de datos MySQL.
3. **Realizar migraciones**: Ejecuta los comandos de migración para crear las tablas en la base de datos MySQL según los modelos definidos en Django.

### 2. Módulo para gestión de usuarios
#### Herramientas
- Django
- Django Rest Framework
- Librería SimpleJWT para manejo de JSON Web Tokens

#### Proceso

##### 2.1 Método para creación de usuario
1. **Definir el modelo de usuario**: Crea o extiende un modelo de usuario en Django para incluir campos como nombre de usuario, correo electrónico y contraseña.
2. **Crear un serializer**: Diseña un serializer para convertir los datos del modelo de usuario a un formato adecuado para la API y viceversa.
3. **Implementar una vista para la creación de usuarios**: Establece una vista que permita la creación de nuevos usuarios a través de la API utilizando el serializer definido.

##### 2.2 Método para Login
1. **Configurar SimpleJWT**: Instala y configura SimpleJWT para la generación y manejo de tokens de autenticación.
2. **Implementar vistas para obtener y refrescar tokens**: Crea las vistas necesarias para que los usuarios puedan obtener un token al iniciar sesión y refrescar el token cuando sea necesario.

##### 2.3 Método para Logout
1. **Crear una vista para Logout**: Implementa una vista que permita a los usuarios cerrar sesión eliminando su token de autenticación.
2. **Agregar la ruta para Logout**: Define una URL en tu API que permita a los usuarios acceder a la funcionalidad de cierre de sesión.

##### 2.4 Método para utilización de JSON Web Token en autenticación
1. **Configurar el sistema de autenticación en Django**: Ajusta la configuración de Django para usar JWT como método de autenticación en lugar del sistema de autenticación por defecto.

##### 2.5 Modelo de datos
1. **Definir el modelo de datos**: Asegúrate de que el modelo de usuario incluya los campos requeridos, como nombre de usuario, correo electrónico, y contraseña.

