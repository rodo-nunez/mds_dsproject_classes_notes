- [Disclaimer!!](#disclaimer)
- [Introducción](#introducción)
  - [Git es un sistema de control de versiones](#git-es-un-sistema-de-control-de-versiones)
  - [Un poquito de historia…](#un-poquito-de-historia)
  - [Un día en la vida de un data scientist](#un-día-en-la-vida-de-un-data-scientist)
  - [Objetivo](#objetivo)
- [El commit](#el-commit)
- [Clone, commit, push, fetch, pull](#clone-commit-push-fetch-pull)
- [Set-up](#set-up)
  - [Checkout](#checkout)
  - [SourceTree](#sourcetree)
- [División de trabajo](#división-de-trabajo)
  - [Trabajo aislado](#trabajo-aislado)
- [Uniendo las piezas](#uniendo-las-piezas)
  - [Commitar versión](#commitar-versión)
  - [Agregar código al index (o staging area)](#agregar-código-al-index-o-staging-area)
  - [Push… y pull!!](#push-y-pull)
- [Demostración en consola vs SourceTree](#demostración-en-consola-vs-sourcetree)
- [Detalles sobre clone, init y origin](#detalles-sobre-clone-init-y-origin)
- [Testeo](#testeo)
- [Ramas](#ramas)
  - [Qué son las ramas y su diferencia con los tags , hash de commits y HEAD](#qué-son-las-ramas-y-su-diferencia-con-los-tags--hash-de-commits-y-head)
  - [Comenzar una nueva parte del trabajo](#comenzar-una-nueva-parte-del-trabajo)
  - [Git Flow](#git-flow)
  - [Mezclando código](#mezclando-código)
  - [Rompiéndolo todo](#rompiéndolo-todo)
  - [Quién gana?! D=](#quién-gana-d)
  - [A solucionar los problemas](#a-solucionar-los-problemas)
  - [Testeo](#testeo-1)
  - [Terminando una sección](#terminando-una-sección)
  - [Inspeccionando un grafo](#inspeccionando-un-grafo)
- [Buenas prácticas](#buenas-prácticas)
  - [Versiones y tags](#versiones-y-tags)
    - [Ejemplo](#ejemplo)
  - [Guía de estilo para commits](#guía-de-estilo-para-commits)
    - [Reglas de estilo para un mensaje de commit genial](#reglas-de-estilo-para-un-mensaje-de-commit-genial)
    - [Los tipos de commit](#los-tipos-de-commit)
  - [README.md](#readmemd)
- [Alias](#alias)
- [Saludos!](#saludos)
- [Referencias](#referencias)

![](pictures/git.jpeg)

# Disclaimer!!

Este taller asume un conocimiento mímino de Git y haber instalado Git,
Git Bash, SourceTree o su herramienta favorita para usar Git. Si no
cumples con estos requerimientos, anda directo a las referencias del
final y ve algunos vídeos en YouTube.

Cada uno tendrá un post-it rosado y otro celeste. Si tienen problemas
peguen el rosado en la parte trasera de sus PCs y los iremos a ayudar.
Si Están listos peguen el celeste, así los que tengan problemas podrán
preguntarles.

> Conversa con tus vecinos de mesa y haz un sondeo de qué tanto sabe
> cada uno de Git. A veces la mejor persona para ayudarte es la que está
> al lado tuyo. (30 seg)

# Introducción

## Git es un sistema de control de versiones

El control de versiones es un sistema que registra los cambios
realizados sobre un archivo o conjunto de archivos a lo largo del
tiempo, de modo que puedas recuperar versiones específicas más adelante.

![](pictures/tv__control-versiones__prehistoria.png)

Esto, ineficiente, también es un control de versiones

## Un poquito de historia…

Linus Torvalds, el creador de Linux, despues de que el proyecto del
Kernel captara grán interés se vio en la necesidad de crear un sistema
que pudiese permitir el trabajo colaborativo (al ser open-source) y que
fuera rápido y eficiente.

**Link:** <https://www.kernel.org/>

![](pictures/windows-build-using-git.jpg)

## Un día en la vida de un data scientist

Como data scientist, aparte de ser **“rápidos y eficientes”** existe
otra característica deseable y es que los análisis, modelos u otros sean
reproducibles. Esto quiere decir que los resultados que pueden ser
replicados sin mayor complejidad si es que se lo requiere.

![](pictures/Knowledge-repository-v2.png)

Airbnb posee lo que se llama un knowkledge repo, donde cada resultado es
almacenado en un repositorio central donde todos los actores relevantes
tienen acceso para seguir explorando y consumirlo

## Objetivo

Introducirlos en el mundo de git y poder enseñarles un flujo de trabajo
con git que nos permita ser eficientes, rápidos y que sea reproducible

Para poder incentivar este flujo de trabajo primero vamos a volver a lo
básico …

# El commit

Si alguna vez has hecho algo en git de seguro viste numeros como
**24b9da6552252987aa493b52f8696cd6d3b00373** en todos lados. Esto es por
que Git guarda utilizando una suma de comprobación que se conoce como
hash SHA-1 (esto tiene que ver con bitcoins 😱)

![](pictures/commit_flujo.png)

Como se ve en la imagen un commit es basicamente una foto instantánea de
los archivos en el momento de hacer el commit que va usualmente
acompañado de un mensaje para indicar que fue lo que se realizó.

# Clone, commit, push, fetch, pull

Vamos a lograr entender esto:

<figure>
<img src="pictures/basic-remote-workflow.png"
alt="Flujo de trabajo con Git" />
<figcaption aria-hidden="true">Flujo de trabajo con Git</figcaption>
</figure>

> Conversen con sus compañeros cuál es la diferencia entre clone, push,
> fetch, pull, commit, working copy, staging area, local repository,
> remote repository.

# Set-up

Creen una carpeta con el nombre workshop\_git, seleccionen clone en la
parte superior. Donde indica *Source Path/URL:* poner el siguiente link

`https://username@bitbucket.org/USER/git-workshop.git`

Donde dice “username” es su usuario de bitbucket. Luego, en *Destination
Path* seleccionar la carpeta recien creada

La dirección del link la pueden sacar directamente de los repositorios
de los proyectos <https://bitbucket.org/USER/git-workshop/src/master/>

## Checkout

Primero en el *History* buesque en el grafo, donde dice
origin/estado\_inicial, y otros tags aprieten click derecho y
seleccionen branch. Ahora, poner un nombre como grupo-N donde N es el
número de su grupo (O inventen sus propios nombres si se sienten
creativos 😎) y darle a *create-branch*.

## SourceTree

<figure>
<img src="pictures/SourceTree.PNG" alt="Así se ve SourceTree." />
<figcaption aria-hidden="true">Así se ve SourceTree.</figcaption>
</figure>

> Comenta con tus compañeros qué información vez en la imagen que no
> sabes qué es y traten de llenar vacíos entre ustedes.

# División de trabajo

## Trabajo aislado

Ejercicio de 3 personas:

-   La <b>persona 1</b> debe: ir la carpeta functions/src y hay un
    archivo llamado “suma.R”. En esta escribir una función
    <b>`suma(x,y)`</b> y que calcule la suma corriente en los reales de
    `x` e `y`

    suma = function(x,y){ 
      r = x+y 
      return(r)
    }

-   La <b>persona 2</b> debe: ir la carpeta functions/src “mult.R”. En
    esta escribir una función <b>`mult(x,y)`</b> y que calcule la
    multiplicación corriente con la suma asociada. Para este ejercicio
    nos restringiremos a la multiplicación de un real por un natural sin
    incluir 0.

<table>
<tbody>
<tr class="odd">
<td>Idealmente la función debe depender de la función suma, si es muy
complicado, solo usar “*”</td>
</tr>
</tbody>
</table>

    mult = function(x,y){
      r = x
      i = 1
      while(i<y){
        r = suma(r,x)
        i = i+1
      }
      return(r)
    }

-   La <b>persona 3</b> debe: Crear un archivo <b>`main.R`</b> que
    cargue ambas funciones (sin copiar y pegar, sino que con la funcion
    `source()` ) y las llame para verificar que `mult(3,3)` es igual a
    sumar 3 veces 3 usando la funcion suma. Debe devolver un boolean e
    imprimirlo. Guardarlo en la carpeta functions/src

<table>
<tbody>
<tr class="odd">
<td>Si alguien no esta seguro como hacer algun punto, puede pedirle
ayuda a su grupo, pero debe escribirlo en su propio computador sin tener
el código del resto.</td>
</tr>
</tbody>
</table>

-   <b>Si el grupo es de 2 personas</b>, la persona 1 debe hacer la suma
    y la multiplicacion, mientras que la persona 2 debe hacer el main.


    source(file = "src/functions/suma.R")
    source(file = "src/functions/mult.R")

    res.mult = mult(3,2)
    res.suma = suma(3,3)

    res.mult == res.suma

    res.mult = mult(3,3)
    res.suma = suma(suma(3,3),3)

    res.mult == res.suma

    res.mult = mult(2,2)
    res.suma = suma(2,2)

    res.mult == res.suma

> A trabajar!! Cada grupo usando su propia rama!

# Uniendo las piezas

## Commitar versión

Para guardar la version actual, debemos hacer un commit y agregarle un
mensaje.

> -   Hagan un <b>commit</b>… qué pasa? Salió bien? Hubo algún problema?
>     Falta algo?
> -   Si la respuesta a lo anterior es que sí hubo problemas, ahora
>     hagan el commit como se debe 😜

<https://git-scm.com/docs/git-commit>

## Agregar código al index (o staging area)

Antes de hacer commit, siempre hay que agregar lo que quieren commitar
al index con <b>`add`</b>. Luego de esto, podemos hacer el commit sin
que sea vacío o no tenga lo que queremos respaldar.

Esto es un error muy común, por esto hago énfasis en esto.

<https://git-scm.com/docs/git-add>

## Push… y pull!!

> Para subir código al repositorio, deben hacer un <b>push</b>. Traten
> de hacer uno cada uno cuando esté listo. Es posible que obtengan
> errores por no tener seteada una upstream branch, pero el error les
> dirá qué hacer.

Es probable que algunos tengan problemas. Esto es porque si alguien más
sube cambios, ustedes DEBEN hacer un <b>pull</b> (descargar el último
commit y juntarlo con el código propio) antes de poder hacer un push.
Esto es importante para evitar pisar cambios de otros en la misma linea.
Las diferencias entre el código del repositorio y local se revisan en el
local y después se suben al repositorio.

<https://git-scm.com/docs/git-push>

<https://git-scm.com/docs/git-pull>

Hay veces en que solo quieren descargar el repositorio pero no mezclarlo
con el local (por ejemplo, si uno no quiere juntar el código aún, sino
que quiere mirarlo antes). Para esto se puede usar <b>fetch</b>. Para
juntar dos commit se usa <b>merge</b>. Hacer un pull es lo mismo que
hacer fetch + merge.

<https://git-scm.com/docs/git-http-fetch>

<https://git-scm.com/docs/git-merge>

Hay una forma de saltarse todo esto… básicamente pasar con una
aplanadora por encima de todos… pero no lo hagan…

<figure>
<img src="pictures/XFQLB.jpg" alt="No sean como esta nina" />
<figcaption aria-hidden="true">No sean como esta nina</figcaption>
</figure>

> Lleguen a un paso en que todos tengan el mismo código con las
> contribuciones de todos. Para esto tienen que usar push y pulls.

# Demostración en consola vs SourceTree

Ahora demostraremos cómo hacer todo esto en ambas herramientas.

# Detalles sobre clone, init y origin

A estas alturas se asume que ya lo hicieron, pero es importante recalcar
la importancia del comando <b>clone</b> para copiar un repositorio de
una url.

<https://git-scm.com/docs/git-clone>

Otra opción es hacer un <b>init</b> para inicializar un repositorio
local y después definirle a qué url se quieren subir los commit. Esta
url hay que configurarla como el <b>origin</b>.

<https://git-scm.com/docs/git-init>

<https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes>

# Testeo

> Corren las funciones para todos? El main.R dice arroja TRUE? Si no es
> así, revisar qué está pasando, corregirlo, y subirlo (ya saben, add,
> commit, pull, push)

Un detalle importante es que TIENEN QUE hacer commit antes de un pull, o
Git no los dejará (para no borra los cambios no commitados).

# Ramas

## Qué son las ramas y su diferencia con los tags , hash de commits y HEAD

> Comentalo con tus compañeros, alguno sabe la diferencia entre cada
> uno?

Tanto las ramas, como los hash de commits y los tags son punteros a
algún commit específico. Uno puede borrar ramas y tags sin perder los
cambios que se hicieron (aunque puede haber problemas después de algunos
meses si uno tiene una rama separada del tronco principal y la borra).

Todos los cambios están almacenados en los commits, los punteros se usan
solo para saltar de un commit a otro.

<figure>
<img src="pictures/SourceTree.PNG"
alt="Ejemplo de grafo de commits con ramas, tags y hashes." />
<figcaption aria-hidden="true">Ejemplo de grafo de commits con ramas,
tags y hashes.</figcaption>
</figure>

-   Las **ramas** son punteros móviles, que se van actualizando a medida
    que uno va haciendo cambios. Estas son útiles para mantener el
    rastro de la versión más actualizada del código en una linea de
    trabajo.
-   Los **tags** son punteros inmóviles, que se mantienen siempre en el
    mismo commit independiente de los nuevos commits que se hagan. Estos
    son útiles para recordar versiones importantes del código y poder
    volver a ellas.
-   Los **hash de commit** son punteros inmóviles que cada commit tiene
    y son únicos (o deberían). Son útiles para identificar cada commit
    de manera única.
-   El **HEAD** es un puntero movil que apunta a la punta de la rama en
    la que uno está parado actualmente. Si uno no está parado en ninguna
    rama actualmente, uno puede estar parado en un commit aislado, lo
    que se llama una *detached HEAD*. El HEAD es útil para saber qué
    versión del código uno está viendo actualmente.

## Comenzar una nueva parte del trabajo

Cuando comienzan a trabajar en algo que podría romper el código o es
otra funcionalidad, siempre es bueno EVITAR trabajar en la rama master.

<figure>
<img src="pictures/gitflow-no-commit-to-master.jpg"
alt="Cuando la tentación es fuerte…" />
<figcaption aria-hidden="true">Cuando la tentación es
fuerte…</figcaption>
</figure>

Para esto existen las ramas.

> Creen una nueva rama llamada develop-nombre, donde “nombre” lo
> reemplazan por su propio. Donde la crearon? Lo hicieron todos? Todos
> la ven? Si no, qué deberían hacer para que todos la vean?

En sourceTree automáticamente se te cambia la rama a esta nueva

> Ahora que ya crearon su nueva rama, cambien con doble click entre
> todas las ramas disponibles. También se puede saltar a tags o commit
> específicos.

El comando <b>`checkout`</b> es el que permite estos saltos si lo hacen
por línea de comando. El comando <b> `branch` </b> es para crear ramas y
si se quiere cambiar y crear una rama usar *git checkout -b
nombre\_rama*

<https://git-scm.com/docs/git-checkout>

<https://git-scm.com/docs/git-branch>

## Git Flow

<figure>
<img src="pictures/GitFlow.png" alt="Git Flow" />
<figcaption aria-hidden="true">Git Flow</figcaption>
</figure>

Un Git Flow es un flujo de trabajo estandard para Git. En la imagen de
arriba hay uno estándar, pero nosotros proponemos este con ligeras
modificaciones:

Cada proyecto debe contener al menos dos ramas, master y develop y
existirán dos ramas extras que pueden ser usadas en caso de ser
requeridas, a continuación, una explicación de cada una:

-   **master:** rama principal del proyecto, acá tiene que estar
    etiquetado con un tag cada código funcional que ustedes consideren
    importante. Por defecto versión tres números X.X.X. Esta es la rama
    de release. Más información en la siguiente sección.

-   **develop:** acá es donde vas desarrollando el código realmente.

-   **feature/XXXX:** reservada para nuevas funcionalidades pero que
    sean grandes (sino en develop directamente). Deben ser mergeadas a
    develop. Borrar la rama después del merge a develop.

-   **quick/XXXX:** para pruebas rápidas pudiendo olvidar las buenas
    prácticas en pro de la rapidez. Estas ramas deben borrarse después
    de terminado el análisis. Si es necesario mantener algo del
    desarrollo hecho en esta rama, mergear a develop con un buen commit.
    No abusar de esta rama.

No deben existir ramas con nombres de personas. Las ramas de
feature/XXXX y quick/XXXX, deben tener nombre del tipo de trabajo que se
está haciendo. No importa que una sola persona esté trabajando en esa
rama, eventualmente podría contribuir otro y es importante que la rama
diga qué tipo de trabajo uno está haciendo en ella (master y develop son
claras por sí solas).

Para hacer merge a master se debe utilizar git merge -no-ff \* porque
así la rama solo contiene los commits de versiones. Si hay conflictos en
master, hacer los merge con mucho cuidado.

## Mezclando código

> Vuelvan a la rama de su equipo. Cada uno modifique una linea DISTINTA
> del main.R, probando con distintas pruebas de `f(suma()) == mult()`.
> Por ejemplo, para `mult(3,3)`, `mult(2,2)` y `mult(3,2)`.

> Cada uno suba sus cambios y después de que todos estén listos, bajen
> la versión final. Funciona? Qué pasó?

## Rompiéndolo todo

> Ahora todos (los 3 o los 2) modifiquen la función suma en la misma
> fila, haciendo que suma calcule x+y+n con n un número fijo que cada
> persona debe elegir (y distinto al n de sus compañeros)

## Quién gana?! D=

> Rápidoooo!! El primero que sube su código gana!!…. qué gana??…. el
> honor, por supuesto! =D (y no tener conflictos en su código).

> Los desafortunados que no logren subir su código primero, tendrán que
> hacer un pull y resolver conflictos en el código. Para eso tendrán que
> escojer con qué versión quedarse en cada linea conflictiva (lineas que
> fueron modificadas en el remoto y el local a la vez).

Para esto recomiendo usar un buen editor de texto como VisualStudio Code
o Sublime, que vienen con herramientas que facilitan el tratamiento de
differencias (diff).

Para los <s>masoquistas</s> rudos, pueden ver las diferencias por
consola con <b>diff</b>

<https://git-scm.com/docs/git-diff>

<figure>
<img src="pictures/diffs-everywhere.jpg" alt="Oh, las diferencias" />
<figcaption aria-hidden="true">Oh, las diferencias</figcaption>
</figure>

## A solucionar los problemas

> Ahora solucionen los problemas en grupo, pónganse de acuerdo con qué
> versión quieren dejar y súbanlo (ya saben… add, commit, pull, push)

## Testeo

> Ahora hagan un pull de su nueva versión y verifiquen que todo
> funcione.

## Terminando una sección

Siempre hay que controlar la cantidad de ramas de un repositorio. Es muy
mala práctica que haya muchas ramas, porque en algún momento habrá que
unirlas… y los conflictos podrían ser… complejos…

<figure>
<img src="pictures/baby.png" alt="Cuando todo te sale bien" />
<figcaption aria-hidden="true">Cuando todo te sale bien</figcaption>
</figure>

Recuerden, las ramas se borran pero los commits siguen ahí

<figure>
<img
src="pictures/what-if-i-told-you-that-in-git-branches-and-tags-are-just-pointers-to-commits.jpg"
alt="=O" />
<figcaption aria-hidden="true">=O</figcaption>
</figure>

## Inspeccionando un grafo

> tomemos un tiempo pero analizar el gráfico en sourceTree

# Buenas prácticas

Además del Git Flow ya descrito anteriormente, expondremos otras buenas
prácticas a considerar

## Versiones y tags

Solo la rama master debe tener tags con versiones en el formato X.X.X.
La rama master debe tener siempre una versión que funcione y haga algo
sin errores (en el ideal). Todo el trabajo se hace en otra parte y
cuando ya es funcional, se pasa a la rama master. Esto es
particularmente importante para los modelos en producción.

-   1er número: Revisión mayor (nueva UI, muchas nuevas funcionalidades,
    cambio conceptual, etc).
-   2do número: Revisión menor (quizás un cambio visual específico, una
    nueva funcionalidad, una colección de arreglos de bugs, etc).
-   3er número: Arreglos de bugs, errores de escritura, formato, etc.

Los tags de estos commit deberían tener el código de versión, pero
además, es útil ponerle un texto muy corto que ayude a recordar qué
versión importante del código era esa. Por ejemplo:
`v0.1.2-MVP_con_modelo_XGB_extra`.

> Agreguen un tag a su último código!

<figure>
<img src="pictures/EjemploTag.PNG" alt="Ejemplo de tag" />
<figcaption aria-hidden="true">Ejemplo de tag</figcaption>
</figure>

### Ejemplo

La primera versión con la estructura de carpetas sería la versión 0.1.0.
A medida que uno le vaya agregando nuevas funcionalidades, cada vez que
uno tenga un avance considerable y estable, aumentar el segundo número
en 1 (ejemplo, 0.2.0). Si uno comete un error y tiene que arreglarlo en
la rama master, arreglar el bug/typo/detalle y ponerle aumentar el 3er
número (ejemplo, 0.2.1). El MVP sería la versión 1.0.0. Cada vez que se
desarrolle otro gran hito en cuando a código, se le suma un valor al
primer número (ejemplo, 2.0.0)

Siempre que se le suma al 1er número, el segundo y tercero quedan en 0.
Ej: De 1.2.5 pasamos a 2.0.0. Siempre que se le suma al 2do número, el
tercero queda en 0. Ej: De 1.2.5 pasamos a 1.3.0

Para los proyectos esto es lo ideal para ordenarse con las grandes
versiones y sobre todo útil al pasar a producción y tener que hacer roll
back.

Como mínimo, deben tener tags los commits asociados a:

-   Inicio del proyecto
-   MVP
-   Primera versión productiva

Cada versión productiva con cambios significativos.

Para los package que hagamos, esto es fundamental, y hay que poner la
versión en un lugar específico para que el gestor de packages sepa
cuándo debe actualizar este.

Además, para los package es útil considerar un 4to número por build.
Para más detalles, preguntar a los que desarrollan más activamente los
package.

## Guía de estilo para commits

El commit debe explicar el “qué” y el “por qué” del cambio, no el
“cómo”.

<figure>
<img src="pictures/BadGoodCommit.PNG"
alt="Ejemplo de buen y mal commit" />
<figcaption aria-hidden="true">Ejemplo de buen y mal commit</figcaption>
</figure>

### Reglas de estilo para un mensaje de commit genial

-   Separar título del cuerpo con una línea en blanco. (para commits
    largos)
-   No terminar la linea del título con un punto.
-   Usar mayúsculas adecuadamente (en título y párrafos).
-   Usar imperativo en el título.
-   Poner saltos de línea cada 72 caracteres (aprox) para no tener
    textos muy largos hacia el lado.
-   Usar el cuerpo para explicar qué y por qué hiciste algo.

### Los tipos de commit

El tipo está contenido en el título y puede ser alguno de estos:

-   feat: una nueva feature o funcionalidad
-   fix: un arreglo de bug
-   docs: cambios a la documentación
-   style: cambios al estilo, formato, puntos y comas faltantes, etc. No
    cambia el código funcionalmente.
-   refactor: refactorización de código
-   test: agregarndo test, refactoring test, no hay cambios al código en
    producción.
-   chore: actualizando tareas de la build, configuraciones de manejo de
    package, etc. No hay cambios al código en producción.
-   Wip (work in progress): para guardar una foto del codigo cuando hay
    trabajo en curso.

No importa el estilo, pero si que pertenezca a la “familia” del commit

Fuente: <https://udacity.github.io/git-styleguide/>

## README.md

La idea de utilizar el readme, es que con solo leer esto se pueda
ejecutar de principio a fin el código con todas sus consideraciones. Por
ello, se sugiere que al menos contenga las siguientes secciones:

-   Descripción general: Resumen del objetivo del código y que problema
    está tratando de resolver.
-   Fuentes de datos: Cómo conseguirlas, con qué regularidad (mensual,
    diaria, anual, solo de una vez) y si requiere algún tipo de permisos
    de acceso. Si es necesario, también con quién hay que conseguir los
    datos.
-   Cómo correr el código: Pasos ordenados y consideraciones.  
-   Resultado: Qué se obtiene del código al final y para qué sirve.

Ejemplo corto de README.md

    # Descripción 

    El objetivo de este código es predecir si un cliente de prepago se convertirá en inactivo en el siguiente mes.  

    # Fuentes de datos 

    Todos los datos ocupados son mensuales y corresponden a una ventana de tiempo de 3 meses antes del mes a predecir. Para esto se ocupan datos de ventas (tablas A, B y C del esquema "transacciones"), datos de Redshift (del esquema clientes, tablas Q y W) y datos en Excel(reporte_mensual.xlsx) enviados por Rubén de Call Center (ruben.ejemplo@empresa.cl). 

    # Cómo correr el código: 

    Los script se deben correr en el siguiente orden: 

    Preprocessing/a00_asdf.R 

    Preprocessing/a01_asdf.R 

    Preprocessing/a03_asdf.R 

    Preprocessing/a04_asdf.R 

    Models/b01_asdf.R 

    Models/b02_asdf.R 

    Models/b03_asdf.R 

    Insight/c01_asdf.R 

    Preprocessing/d01_asdf.R 

    Insight/e01_asdf.R 

    O alternativamente, correr código main.R en la carpeta origen del proyecto, que llama a todo el resto de los archivos en orden. 

    # Resultados: 

    El output de este proceso es una tabla de clientes con sus respectivas probabilidades de quedar inactivos, en formato csv, en la ruta files/modeling_output/probabilidades.csv, junto con unos gráficos en la carpeta files/modeling_output_figures y reportes en files/modeling_output/reports. 

# Alias

Los alias son muy útiles para no escribir tanto en la consola. Se pueden
guardar atajos para cualquier tipo de código, largo o corto. Si es algo
que usas (o te gustaría usar) muy seguido, lo más probable es que
deberías crear un alias.

Algunos ejemplos de alias son

    $ git config --global alias.co checkout
    $ git config --global alias.br branch
    $ git config --global alias.ci commit
    $ git config --global alias.st status

Lo que hace el primer comando, es crear una linea en el archivo de
configuración global de git, donde asocia el string `co` al string
`checkout`. Hace un trabajo análogo con las demás. Todo esto agrega esta
sección al archivo `~/.gitconfig` (que suele estar en el home de cada
uno)

        [alias]
            co = checkout
                br = branch
                ci = commit
                st = status

Además, puedes tener alias más largos. Ejecuta esta linea:

`git config --global alias.lg "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative"`

> Luego de ejecutar el comando anterior, ejecutar `git lg` y ver qué
> pasa. Cuál es el resultado de este comando?

Aquí hay una lista de algunos alias que podrían ser útiles. Lo mejor es
ir creandolos uno mismo poco a poco según la necesidad, pero esto les
puede dar algunas ideas:

    [alias]
            lg = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative
            co = checkout
            br = branch
            ci = commit
            st = status
            unstage = reset HEAD --
            last = log -1 HEAD
            ac = !git add -A && git commit -m
            chs = !git checkout $1 && git status
            caa = !git commit -a --amend -C HEAD
            caam = !git commit -a --amend -m
            update = !git fetch --all -p

# Saludos!

Espero que les haya servido el workshop! Hay mucho más que no está
mencionado aquí. El objetivo de este workshop es ayudarles con el
puntapie inicial, pero si quieren aprender más, les recomiendo las
referencias de abajo!!

Abajo les dejo algunas cosas de las que vimos aquí y otras que no, por
si quieren seguir indagando:

-   Entendimiento de qué es y para qué sirve Git

-   Manejo de comando básicos como add, commit, pull, push

-   Checkout para cambiar de ramas o commits.

-   Crear y borrar ramas

-   Saber cómo resolver conflictos simples dejando un archivo completo
    como el definitivo

-   Usar el stash

-   Conocer al menos 3 repositorios de git y principales diferencias
    (ej: GitHub, Bitbucket, GitLab)

-   Conocer alguna GUI para git y saber cómo hacer lo básico en esta
    (push, pull, commit, add). Algunos ejemplos son SourceTree,
    VisualStudio Code, RStudio

-   Saber cómo resolver conflictos no tan básicos linea a linea usando
    el diff de algún editor de texto (por ejemplo el de Visual Studio
    Code)

-   Tags

-   Aliases

-   Buenos mensajes de commit y estilos de commit

# Referencias

-   Git Documentation <https://git-scm.com/doc>

-   Pro Git Book <https://git-scm.com/book/en/v2>

-   What is Git and GitHub?
    <https://www.youtube.com/watch?time_continue=1&v=uUuTYDg9XoI>

-   Learn to Git: Basic Concepts
    <https://www.youtube.com/watch?v=8KCQe9Pm1kg>

-   DataCamp Course
    <https://www.datacamp.com/courses/introduction-to-git-for-data-science>

-   TryGit <https://try.github.io/levels/1/challenges/1>

-   Getting started with Git using SourceTree
    <https://www.youtube.com/watch?v=UD7PV8auGLg>

-   Workshop de Carpentry: El Control de Versiones con Git
    <https://swcarpentry.github.io/git-novice-es/>
