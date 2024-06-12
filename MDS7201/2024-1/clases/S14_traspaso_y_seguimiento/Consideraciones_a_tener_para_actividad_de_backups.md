
Para poder ejecutar un proyecto en menos una mañana, a veces hay que hacer algunos ajustes. Si un proyecto demora 8 horas en correr, no es posible revisarlo en una mañana. Por esto, es importante tener en cuenta las siguientes consideraciones al preparar tu proyecto para la sesión de backups:

1) Partir leyendo el README.md para saber qué hay que ejecutar:

No es necesario leer el README.md del proyecto completo antes de ejecutar el código, pero sí es necesario encontrar en él la información mímina para comenzar la ejecución. El resto lo podrán leer mientras se ejecuta el código.

Estas instrucciones deben ser fáciles de encontrar y deben estar en una sección con un nombre adecuado para que sea fácil de encontrar. Es recomendable decir cuál es esa sección al comienzo del README.md, con algo como "Para leer las instrucciones de ejecución en modo de prueba, ir a la sección X".

2) Ponerse en el lugar de alguien que no conoce nada del proyecto:

Al escribir las insctrucciones de cómo ejecutar el modo de prueba, escribelas como a ti te gustaría que te explicaran un proyecto del que no sabes nada y tienes que ejecutar en 60 minutos. Escribe la información justa y necesaria para poder ejecutar sin problemas.

Luego de escribir esto, lee lo que escribiste, siguelo al pie de la letra, no asumas nada. Si funciona la prueba, genial; si no funciona, preguntate qué falta explicar más o qué deberías modificar en los scripts para facilitar el proceso. Itera hasta que las instrucciones sean a prueba de novatos. 

3) Máximo 60 minutos:

El proyecto debe poder ser ejecutado entero en máximo 60 minutos. El resto del tiempo se ocupará leyendo código, entendiendo la estructura general, evaluando los puntos del manifiesto, etc. Para que otro lo pueda ejecutar en menos de 60 minutos, tú tienes que poder ejecutarlo en menos de 60 minutos. Debes testear esto antes de la sesión de backup.

4) Credenciales necesarias:

El owner debe pasarle las credenciales necesarias para ejecutar el proyecto directamente al backup y NO deben estar comiteadas en bitbucket. Todas las contraseñas deben ser cargadas a mano una única vez en las variables de entorno, ya sea las de R en ~/.Renviron o en las variables de entorno de linux o python.

Si hay credenciales que no pueden ser reveladas al backup, hay que generarle contraseñas personales con los avvesos necesarios. Si no se le pueden generar contraseñas nuevas a tiempo o hay problemas de confidencialidad, debe haber una muestra de los datos que requieren esas credenciales guardada en S3 (en un .rds, .feather, .csv, .pickle, etc).

A veces hay problemas de VPN o se necesita hacer tunneling. Si ese proceso no está automatizado, también es mejor dejar archivos en S3 en vez de leer datos de bases de datos o servidores. 

Recuerden que no basta con solo dejar archivos en S3, hay que modificar el proyecto para ir a leer esos archivos en la rama "modo_de_prueba" para que quede todo listo para correr. 

A veces uno tiene todas las credenciales necesarias, pero las lecturas de bases de datos son lentas. En estos casos igual es recomendable usar archivos en un .rds, .feather, .csv, .pickle, etc para evitar largos tiempos de espera en las pruebas.

5) Debe ser fácil entrar en modo de pruebas:

Independiente de lo anterior es recomendable tener una forma de correr fácilmente el proyecto en modo de prueba, es decir, usar los datos fundamentales para testear si el proyecto funciona o no.  

Es bueno tener un parámetro en el pipeline para entrar en este modo de prueba y leer solamente las n primeras filas de una base de datos o leer un archivo en vez de acceder a la base de datos, etc.

6) Ejecutar en rama "master" o "modo_de_prueba":

Recuerden que la versión oficial a testear siempre será "master" a menos que el README.md de "master" indique lo contrario.

Si el proyecto demora más de 60 minutos, es fundamental que el código a evaluar por el backup esté en una rama especial llamada "modo_de_prueba" que sale de "master" y tiene las adaptaciones necesarias para que las pruebas demoren poco. Esto es inependiente de si el proyecto tiene un parámetro para ponerlo en modo de pruebas o no. 

El nombre de la rama "modo_de_prueba" puede variar, pero debe estar siempre documentado en "master". 

7) En caso de tener varios pipeline, especificar cuales hay que testear:

A veces uno tiene muchos pipelines con objetivos distintos. En el README.md de la carpeta pipeline debe estar bien documentado cuál es el objetivo de cada pipeline y en el README.md del proyecto general debe decir cuales de esos pilepine son los fundamentales y deben ser testeados. Quizás es solo 1, quizás son más. Como sea, debe decir explícitamente cuales son los fundamentales y el tiempo de ejecición de la suma de ellos debe ser máximo 60 minutos en modo de prueba. 

Además de lo que debería estar en el README.md, compartiremos una planilla donde explicitaremos (de manera colaborativa) que scripts se deben ejecutar en cada proyecto. Esto lo debe llenar cada owner del proyecto.

8) Rubrica de evaluación:

Mientras esperas que corra el código, revisa los scripts siguiendo la rubrica de evaluación que entregaremos. 