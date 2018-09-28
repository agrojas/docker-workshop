# Apache example
Ejemplo donde se levanta un container donde se ejecuta un apache y se comparte un directorio mediante el uso de un volumen

#### Clonar proyecto
```
git clone git@github.com:agrojas/docker-workshop.git
cd docker-workshop/examples/apache-example
```

#### Descargar imagen de apache

```
docker pull httpd
```


#### Correr el container y visualizar el contenido estatico

Correr un container con la imagen del apache utilizando el flag **--name** y el nombre __apache_volume_example__
A su vez se asocia el directorio donde se ejecute el comando **$(pwd)** con el directorio **/var/www/** del container mediante el flag **-v**

```
docker run --name apache_volume_example \
           -p 8180:80 -p 443:443 \
           -v $(pwd):/var/www/ \
           -d httpd
```

__Abrir http://localhost:8180__

#### Realizar cambios
Modificar el archivo html/index.html de manera local y verificar los cambios en http://localhost:8180

