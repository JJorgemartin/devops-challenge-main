# Craftech Challenge - Prueba 2
## Despliegue de una aplicacion Django y React.js

## Tabla de contenidos
***
1. [Informacion general](#informacion-general)
2. [Tecnologias](#tecnologias)
3. [Instalacion en PC Local](#instalacion-en-pc-local)
4. [Instalacion en Nube](#instalacion-en-nube)


## Informacion general
***
Challenge para el puesto de DevOps creado por la empresa Craftech. Se solicita lo siguiente:
* Elaborar el deployment dockerizado de una aplicacion django(backend) con frontend en React.js. Desplegar todos los servicios en un solo docker-compose
* Subir las instrucciones detalladas para compilar y desplegar la aplicacion, tanto en una PC local como en una nube. (AWS o GCP)


## Tecnologias 

***
Lista de las tecnologias que se utilizaron en el proyecto:
* [Python](https://www.python.org/): Version 3.7.14
* [Node](https://example.com): Version 8.16
* [Django](https://www.djangoproject.com/)
* [React.js](https://es.reactjs.org/)


## Instalacion en PC Local 

***
A cerca de la instalacion en PC local. Corroborar tener instalado [Docker](https://www.docker.com/)  y [docker-compose](https://docs.docker.com/compose/install/).  
```
$ git clone https://example.com
$ cd ../path/to/the/file
$ docker-compose up
```

## Instalacion en Nube
***

Se elige **AWS** como nube para el ejemplo. Vamos a suponer que no tenemos ninguna instancia levantada, en ese caso procedemos a levantar una instancia desde EC2. Elegimos el AMI correspondiente, que puede ser un Ubuntu 20.01 y se procede a elegir el hardware de la misma, puede ser un t2.micro, una vez lanzada la instancia vamos a proceder a copiar el ip public para entrar a la misma a traves del comando ssh.
```
$ ssh -i nombre ubuntu@[IP]
```
Luego de entrar a la instancia. 
```
$ sudo apt-get update
$ sudo apt-get install docker.io docker-compose
```

Procedemos a clonar el repositorio dentro de la instancia con:
```
$ git clone https://example.com
```

Y por ultimo levantamos el contedor con docker-compose:
```
$ docker-compose up
```

