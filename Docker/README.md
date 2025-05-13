# Proceso de Creación y Despliegue de Imagen Docker
## 1. Preparación Inicial
Para comenzar el proceso de despliegue, primero se organizó la estructura del proyecto con sus archivos necesarios: el código de la aplicación, archivos de configuración y dependencias.

## 2. Configuración de Docker
Se creó el archivo Dockerfile en la raíz del proyecto con las instrucciones necesarias para construir la imagen, incluyendo la instalación de dependencias y la configuración del entorno.

## 3. Proceso de Despliegue
### 3.1 Autenticación
Primero se realizó la autenticación en Docker Hub:

- Se ejecutó el comando docker login
- Se ingresaron las credenciales (usuario: Mi_Usuario)
- Se verificó el mensaje de "Login Succeeded"
### 3.2 Construcción de la Imagen
Se construyó la imagen local:

- Se navegó al directorio del proyecto
- Se ejecutó el comando de construcción: docker build -t navegaciontuberiafiltro .
- Se esperó a que completara el proceso de construcción
### 3.3 Etiquetado
Se etiquetó la imagen para subirla a Docker Hub:

- Se utilizó el comando: docker tag navegaciontuberiafiltro Mi_Usuario/navegaciontuberiafiltro:latest
- Esto preparó la imagen para su subida al repositorio
### 3.4 Subida a Docker Hub
Se subió la imagen al repositorio:

- Se ejecutó: docker push Mi_Usuario/navegaciontuberiafiltro:latest
- Se monitoreó el progreso de la subida
- Se verificó la finalización exitosa
## 4. Verificación
Para comprobar el despliegue exitoso:~

- Se descargó la imagen: docker pull Mi_Usuario/navegaciontuberiafiltro:latest
- Se ejecutó localmente: docker run -p 5000:5000 Mi_Usuario/navegaciontuberiafiltro:latest
- Se verificó el acceso a través del navegador en http://localhost:5000
## 5. Resultado Final
La imagen quedó disponible públicamente en Docker Hub, permitiendo que cualquier usuario pueda descargarla y ejecutarla siguiendo los comandos de instalación y ejecución proporcionados.