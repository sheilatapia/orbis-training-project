# Capacitación: Docker
Integrantes:
- Sheila Tapia
- Cesar Casanova

# Preguntas

## PARTE 4
1. ¿Qué importancia tiene los tags en un proyecto?
Los tags son versiones de un proyecto e informa 

2. ¿Cuál es la diferencia entre un tag normal y un tag anotado en git?
Para crear un tag anotado se utiliza el flag -a, al cual se le debe agregar una descripción.

3. ¿Cómo se sube todos los tags de git que hay en mi local?
Usando el comando: git push --tags 

4. ¿Es necesario loguearse cada vez que subo una imagen a dockerhub?
Basta con loguearse la primera vez que se subirá una imagen a dockerhub (usando docker login -u [usuario]) sin embargo no es necesario loguearse cada vez que se suba una imagen.

5. ¿Qué es y para qué sirve docker?
ES una herramienta que permite alojar aplicaciones, libs, etc. de manera isolada para que el usuario pueda transportarlo y mejore el trabajo.

6. ¿Cuál es la diferencia entre docker y VirtualBox (virtualización)?
- Docker no requiere un so instalado, usa el so que usa su cliente/host
- Un contenedor de docker es mas ligero, porque usa los recurso basicos del kernel que no cambian de una pc a otra.

7. ¿Es necesario depender de una imagen de docker base al crear una imagen nueva?
Es necesario extender de una imagen padre (scratch)

8. ¿Por qué debo anteponer el nombre de usuario en una imagen docker nueva?
Porque docker debe saber a que docker hub va  pushear

9. ¿Que pasa si creo una imagen sin especificar una versión o tag, con qué versión se crea?
Se crea con 'latest'

## PARTE 5
¿Porqué es necesario crear un contenedor con esta bandera -it ? ¿Qué pasa si no le pongo -it?
Para que puedas interactuar con el contenedor y puedas acceder al terminarl. Si no coloco el flag -it, el contenedo se crea pero no podré interactuar con el.

¿Para qué sirve ejecutar el comando bash al ejecutar una imagen?
Sirve para que devuelva un terminar con el cual interactuar


¿Cuál es la diferencia entre docker ps y docker ps -a?
Docker ps : lista todos los contenedores encendidos
docker ps -a: lista todos los contenedores.

Ejecutar el contenedor:
docker run -it --rm sheilatapia/orbis-training-docker:0.2.0 bash

1. ¿Cuál es la diferencia entre una imagen y un contenedor?
El contenedor es contruído en base a una imagen, el contenedor puede convertirse en una imágen posteriormente.

2. ¿Cómo listo las imágenes que hay en mi computadora?
docker images 

3. ¿Cómo salgo de un contenedor de docker?
exit

4. ¿Se elimina el contenedor al salir de ella?
No, a menos que se le hya indicado al inicializar el contendor

5. ¿Cómo elimino un contenedor?
docker rm [nombre-del-contenedor] -f

6. ¿Para qué es necesario el flag `-i`, `-t`, `--rm`?
'-i'   : Es interactivo
'-t'   : Abre el terminal
'--rm' : Elimina automaticamente el contenedor al salir de el

7. ¿Cómo verifico que el archivo creado se encuentra en la imagen?
Colocando en el dockerfile lo siguiente: RUN ls /app

8. ¿Cómo se comenta una linea de código en Dockerfile?
Colocando lo siguiente antes del comentario: "#"

## PARTE 6

1. ¿Qué es NGINX?
Es un servicio web que te permite alojar y ejecutar aplicaciones web, en lenguajes como PHP-NODE-PYTHON

2. ¿Cómo expongo puertos en docker?
docker run --expose 80 sheilatapia/orbis-training-docker:1.0.0 bash

3. ¿Cómo especifico los puertos al levantar un contenedor (docker run)?
docker run -p 1080:80 sheilatapia/orbis-training-docker:1.0.0 bash

4. ¿Cómo hago 'forward' al levantar un contenedor (docker run)?
docker run -p 192.168.1.2:1080:80 sheilatapia/orbis-training-docker:1.0.0 bash