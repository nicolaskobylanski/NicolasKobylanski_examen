# Examen Nicolás Kobylanski
### Link repositorio de GitHub: [https://github.com/nicolaskobylanski/NicolasKobylanski_examen]

*1º Explica que es un “Pull Request” en Github. (1 pts)*

- Un "Pull Request" en Github se da cuando primeramente un usuario realiza un fork de un repositorio del cual no es dueño. El usuario que realiza el fork, realiza ciertas modificaciones al repositiorio de manera local (en su máquina), y una vez finalizadas las modificaciones, el usuario puede enviar al dueño un Pull Request de dicho repositorio con las modificaciones realizadas. Si el Pull Request es aceptado, los cambios realizados por el usuario ajeno se integrarán en el repositorio original.

*2º ¿Qué es un conflicto de fusión (merge conflict) en Git? Explica como resolverías este conflicto. (1 pts)*

- Un conflicto de fusión en Git se da cuando un usuario trata de fusionar dos ramas para integrar diferentes cambios de una rama en la otra. Al realizar esta integración, lo más común es que surjan errores, conocidos como "merge conflict". La máquina trata de fusionar dos ramas, pero no es capaz de hacerlo de manera perfecta, por lo tanto, los errores tienen que ser solucionados manualmente. Para solucionar los diferentes conflictos se debe entrar en los archivos con conflictos mediante el comando **nano <nombre_archivo>**. Una vez dentro del archivo se eliminarán todos los errores (código duplicado, caracteres de más, étc...). Cuando se hayan eliminado los errores se cerrará el editor VI y se guardarán los cambios. Habrá que utilizar el comando **git add .** para confirmar los cambios y añadir los archivos modificados, y a continuación el comando **git merge --continue** para continuar y finalizar el merge.

*3º Imaginemos que tenemos dos ramas, la principal llamada “main” y la rama “examen_parcial”. ¿Qué procedimiento se debería seguir para fusionar (merge) ambas ramas? (0.5 pts)*

- El primer paso para fusionar o "mergear" ambas ramas es elegir cual queremos fusionar primero (en este caso, elijamos "main" en "examen_parcial", y después "examen_parcial" en "main"). Una vez elegida la rama, deberemos asegurarnos de que nos encontramos dentro de ella. Para ello, utilizaremos un comando para navegar entre ramas: **git checkout main**. Una vez dentro de "main", introduciremos el comando **git merge examen_parcial**. Surgirán conflictos y deberemos solucionarlos (explicado anteriormente en el ejercicio 3). Una vez finalizado este merge, nos cambiaremos a la rama "examen_parcial", con el comando: **git checkout examen_parcial**, y realizaremos los mismo pero con la rama "main": **git merge main**, y una vez más solucionaremos conflictos si es que surgen.

*4º Has realizado un commit, pero luego descubres un error importante en los cambios que has incluido. Necesitas revertir este último commit para regresar tu proyecto al estado anterior, pero deseas mantener los cambios realizados en tu área de trabajo. Explica el comando de Git que utilizarías para llevar a cabo esta acción. (0.5 pts)*

- Para revertir un commit utilizaría en primer lugar el comando **git reset --hard HEAD~1** este comando eliminaría las modificaciones realizadas en el último commit. Si se desease eliminar más de un commit, tan sólo habría que modificar el "HEAD~1" del comando, sustituyendo el número 1 por la cantidad de commits que se desearían eliminar.

*5º ¿Cómo se realiza un fork de un repositorio en GitHub y para qué se utiliza comúnmente esta acción? (1 pts).*

- Para realizar un fork en GitHub, el usuario elige un repositorio ajeno el cual desea modificar. Una vez elegido el repositorio, se pulsa el botón de **fork** dentro del repositorio. Esto creará una copia exacta en el repositorio remoto (la "nube", en este caso, GitHub) del usuario. Esta acción se utiliza comúnmente para modificar y contribuir a otros repositorios. Es importante destacar que los cambios que realice el usuario sobre esta copia del repositorio no se aplicarán al original, a menos que se realice un Pull Request (preg. 1), y sea aceptado por el dueño del repositorio original.
  

*6º Te encuentras trabajando en un proyecto y necesitas llegar a un archivo específico llamado "archivo.txt". Este archivo está ubicado dentro de una estructura de directorios en tu sistema.*

*a) Desde tu posición actual en el directorio raíz (home) de tu proyecto, ¿cómo llegarías al directorio que contiene "archivo.txt", el cual está dentro del directorio "UAX", el cual a su vez está dentro del directorio "Universidad", que se encuentra dentro del directorio "Nombre_del_alumno (raíz)"? Proporciona el comando exacto que usarías y especifica qué tipo de ruta es. (0.5 pts)*

- Para llegar al directorio que contiene a "archivo.txt" se utilizaría el comando **cd .** para navegar entre directorios. En este caso se utilizaría de esta manera: **cd /Nicolás_Kobylanski/Universidad/UAX**, el cual nos llevaría directamente al directorio UAX, y si se utiliza el comando **ls** nos mostraría los contenidos; "archivo.txt". La ruta se trata de tipo absoluto, pues al encontrarnos en el directorio raíz, deberíamos pasar por todos los directorios para llegar a nuestro destino.

*b) Si te encuentras actualmente dentro del directorio "Universidad", ¿cómo accederías al directorio que contiene "archivo.txt"? Proporciona el comando exacto que usarías y especifica qué tipo de ruta es. (0.5 pts)*

- Para llegar al directorio **UAX** desde el directorio **Universidad**, bastaría con introducir el comando **cd UAX**. Se trataría de una ruta relativa, pues no nos encontramos en el directorio raíz y el directorio **UAX** está contenido dentro de **Universidad**.

*7º Te han asignado la tarea de trabajar en un proyecto de código abierto alojado en GitHub. Como nuevo colaborador, se espera que sigas las mejores prácticas para el manejo del código fuente utilizando Git. Que comandos de Git utilizaría para las siguientes tareas: (2 pts) (0.2 cada pregunta):*

*1) Clonar el Repositorio:*

~~a) git pull~~

**b) git clone**

~~c) git fetch~~

~~d) git branch~~

*2) Crear una Nueva Rama:*

**a) git branch**

~~b) git checkout~~

~~c) git merge~~

~~d) git add~~

*3) Cambiar entre Ramas:*

~~a) git merge~~

~~b) git branch~~

**c) git checkout**

~~d) git pull~~

*4) Añadir Cambios al Área de Preparación (Staging):*

~~a) git commit~~

**b) git add**

~~c) git push~~

~~d) git checkout~~

*5) Realizar un Commit:*

~~a) git add~~

**b) git commit**

~~c) git push~~

~~d) git merge~~

*6) Publicar la Rama en el Repositorio Remoto:*

~~a) git pull~~

**b) git push**

~~c) git merge~~

~~d) git branch~~

*7) Actualizar tu Rama Local con Cambios del Remoto:*

~~a) git push~~

~~b) git branch~~

**c) git pull**

~~d) git checkout~~

*8) Fusionar Cambios de otra Rama a tu Rama Actual:*

~~a) git checkout~~

~~b) git branch~~

~~c) git pull~~

**d) git merge**

*9) Revertir Cambios Locales:*

**a) git reset --hard**

~~b) git pull~~

~~c) git merge~~

~~d) git branch~~

*10) Revisar el Historial de Commits:*

~~a) git commit~~

~~b) git push~~

**c) git log**

~~d) git add~~

*8º Describe detalladamente los pasos y consideraciones que tomarías para lograr esta tarea, incluyendo cómo manejarías los posibles conflictos de fusión y cómo asegurarías que la integración final en develop sea estable y funcional. (2 pts)*

- El primer paso a llevar a cabo sería fusionar la rama de **matemáticas** en la rama **develop**. Se debería de integrar primero esta rama pues la algoritmia (o el back-end del proyecto) necesita estar terminado y ser estable para que al integrar la rama de Diseño UX (front-end del proyecto) no se generen un exceso de conflictos. Es decir, para que el equipo que trabaja en la parte de diseño tenga en cuenta todas las modificaciones que realice la parte de matemáticas antes de integrarse en **develop**. Si se tratase de integrar tanto **Diseño UX** como **matemáticas** al mismo tiempo en **develop**, se generarían más conflictos que si se hubiese integrado una rama antes que la otra, pues se hubiesen podido considerar las modificaciones de cada equipo y realizar los cambios oportunos antes de integrarse. Alternativamente, se podría realizar una fusión de la rama **Diseño UX** y **matemáticas** como una sola antes de integrarla en **develop**. A nivel técnico, la integración se realizaría de esta manera:

   **git checkout develop** Nos cambiamos a la rama develop
  
   **git merge mátematicas** Comenzamos el merge de matemáticas
  
   **nano <archivos_con_conflictos>** Nos metemos en los que generen conflictos, y se solucionan entre miembros del equipo develop y matemáticas
  
   **git add .** Se añaden los cambios
  
   **git merge --continue** Se finaliza la fusión
  

- A continuación se realizaría lo mismo pero con la rama **Diseño UX**, y a la hora de corregir conflictos se haría entre miembros de todos los equipos para evitar confusiones entre ramas. Una vez finalizado el merge entre las tres ramas dentro de **develop**, y todos los conflictos solucionados, el proyecto estaría listo para ser enviado a la rama **main**.

*9º Pregunta práctica del módulo 3: Repositorios local y remoto*

*Recientemente, has completado una práctica en la que creaste un repositorio tanto local como remoto para una calculadora web sencilla. La práctica implicaba varios pasos clave, incluyendo la creación del repositorio, la adición y el registro de cambios, y finalmente la subida del repositorio local al remoto en GitHub.*


*Considerando los pasos realizados durante la práctica, responde la siguiente pregunta:*

*¿Cuál de las siguientes afirmaciones describe mejor el proceso que seguiste para añadir el botón de "x^4" a tu calculadora web y subir los cambios al repositorio remoto? (1 pts)*

*Opciones:*

~~A) Editaste directamente el archivo "index.html" en GitHub y creaste un nuevo commit en la rama principal (master).~~

~~B) Clonaste el repositorio remoto, hiciste cambios en el archivo "index.html" en una rama secundaria, y luego hiciste un pull request a la rama principal (master).~~

**C) Añadiste el botón "x^4" al archivo "index.html" en tu repositorio local, creaste un commit con los cambios y luego subiste el repositorio local al remoto en la rama principal (master).**

~~D) Creaste un nuevo archivo para el botón "x^4", lo añadiste al índice en tu repositorio local, pero no creaste un commit ni subiste los cambios al repositorio remoto.~~



     
