#Prueba 2

+ Se realiza la prueba de manera local.
+ Se generan un directorio para el proyecto y se coloca los archivos del backend (código de Django) y del frontend (código de React.js) en sus respectivas carpetas.
+ Se crea un archivo Dockerfile en la raíz del proyecto para el backend (Django) donde se define la imagen base (python:3.7), se copian los archivos del proyecto, se instalan las dependencias, se expone el puerto 8000 y se configuran los comandos necesarios para ejecutar el servidor de Django. Se presentan inconvenientes para que el código identifique la secret key, se genera archivo .env donde se agrega dicha información.  
+ Se crea otro archivo Dockerfile en la raíz del proyecto para el frontend (React.js). donde se define la imagen base (node:alpine3.15), se copian los archivos del proyecto, se instalan las dependencias y se configurar los comandos necesarios para compilar y servir la aplicación de React.js.
