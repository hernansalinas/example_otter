El otter es muy sensible a la sintexis que se emplea, cual fallo en espacio, puede dar lugar a problemas con el otter. 
Por eso se reomienda seguir en detalle su sintaxi para tener exito, al principio es engorro pero cuando se pone a punto 
funciona muy bien. Este guia esta realizada para trabajar con otter en local. 

En un notebook,  todo pregunta con en el otter debe empezar con una tipo Manual, si no se empieza con este tipo de pregunta
la generacion del archivo zip y pdf para el estudiante puede traer problemas, cuando se tiene el notebook listo se debe 
ejecutar los siguientes comandos: 


otter assign test.ipynb dist/

Lo anterior generara dentro de dist, si todo va bien, dos directorios:
	
	- El primero tiene el notebook del estudiantes
	- El segundo el aurograder con archivos zip y test con la solución.
  
para calificar el notebook del estudiante en local bastará con ejecutar :

	- otter run -a autograder.zip test.ipynb > output

En este ejemplo, he traido el archivo .zip con el nombre aurograder al directorio donde estoy trabajando y el archivo test.ipynb qeu se
corresponde a la solución del estudiante en el mismo, la salida la escribo en un archivo .output. Este archivo queda listo para que se puedan 
generar reportes para el estudiante de las notas de su notebook


Las pruebas de este directorio estan realizadas para: 
1. Estudiante que falla todo el test 
2. Estudiante que no ingresa todoas las preguntas, en este caso el nombre
3. Estudiante que primero falla el notebook y despues hace todo ok: Hay que estar muy atento en esta parte por que se cargan variables en memoria, que hace 
que asi el notebook este ok, la ultima parte falla. Lo anterior sucede, cuando se modifica el notebook y después se vuelve a modificar el submision carga el estado 
anterior

En submission, creo una copia de cada notebook para realizar el respectivo test e informe de otter
