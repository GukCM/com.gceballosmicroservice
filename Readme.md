Requisitos: 
*Tener instalado maven y java con sus respectivas variables de entorno

Para correr el proyecto en local, dirigirse a la carpeta raiz del proyecto C:/..../gusgus y utilizar el comando en terminal: ./mvnw spring-boot:run

Despues dirigirse a su navegador y digitar la url "localhost:8080/saludo"

Pasos para utilizar Docker:

Para preparar el jar y subirlo a docker utilizar en terminal dentro de la carpeta raiz: mvn clean package

Para crear el docker con el tag "springservice" utilizar: docker build -t springservice .

Para correr el docker en el puerto 3001:8080/$url utiliza: docker run -it -rm -p 3001:8080 --name myspringservice springservice


mvn clean package: preparar el .jar para subirlo a docker
docker build -t springservice .: crear el docker con el tag de springservice
docker run -it -rm -p 3001:8080 --name myspringservice springservice: correr el docker en el puerto 3001:8080/$url