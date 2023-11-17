# Proyecto Microservicio

Este proyecto consiste en un microservicio que se ejecuta en un contenedor Docker y se despliega en una instancia EC2 de AWS utilizando Terraform.

## Instalación

Para instalar este proyecto, necesitarás tener instalado Docker, AWS CLI y Terraform en tu máquina local.

1. Clona este repositorio en tu máquina local.
2. Configura tus credenciales de AWS utilizando el comando `aws configure`.
3. Navega al directorio del proyecto y ejecuta `terraform init` para inicializar tu entorno de Terraform.

## EL uso

Para desplegar el microservicio, sigue estos pasos:

1. Construye la imagen Docker con el comando `docker build -t calderon07/microservicio .`
2. Sube la imagen a Dockerhub con el comando `docker push calderon07/microservicio`.
3. Ejecuta `terraform apply` para crear la instancia EC2 y desplegar el microservicio.

Una vez que la instancia EC2 esté en funcionamiento, puedes acceder al microservicio navegando a la dirección IP pública de la instancia en un navegador web.

## Funcionamiento

El microservicio se ejecuta en un contenedor Docker en una instancia EC2 de AWS. Utiliza un archivo `Dockerfile` para construir la imagen Docker y un archivo `main.tf` para configurar la infraestructura de AWS con Terraform.

El microservicio está configurado para escuchar en el puerto 80. Cuando se accede al microservicio, devuelve el contenido del archivo `index.html`.

El grupo de seguridad de la instancia EC2 permite el tráfico entrante en el puerto 80 para permitir el acceso al microservicio.

Espero que esto te ayude a entender cómo instalar, usar y entender el funcionamiento de este proyecto. Si tienes alguna pregunta, no dudes en preguntar.