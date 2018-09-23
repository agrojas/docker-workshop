# Run jenkins
Ejemplo de ejecutar un jenkins desde un container

## Descargar imagen
docker pull jenkins/jenkins

## Correr el container
docker run -p 8080:8080 -p 50000:50000 jenkins/jenkins


## Ingresar al jenkins

 -> http://localhost:8080