# Apache example
Ejemplo donde se levanta un container donde se ejecuta un apache. A su vez se asocia el directorio 
donde se ejecute el comando **$(pwd)** con el directorio **/var/www/** del container mediante el flag **-v**

### Clonar proyecto
```
git clone git@github.com:agrojas/docker-workshop.git
cd docker-workshop/examples/apache-example
```

### Descargar imagen de apache

```
docker pull httpd
```

### Correr el container

Correr un container con la imagen del apache utilizando el nombreapache_volume_exampl

```
docker run --name apache_volume_example \
           -p 8180:80 -p 443:443 \
           -v $(pwd):/var/www/ \
           -d httpd
```


// Abrir http://localhost:8180 para ver el archivo html
// Abrir http://localhost:8180 para ver el archivo html

```
