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