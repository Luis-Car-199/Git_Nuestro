Respuestas:


Paso 11 → git reset –hard HEAD~1 porque este comando sirve para deshacer un commit modificando el WC. Se mueve hacia atrás según el numero depues de ~ en este caso como es 1,
se desplaza hasta el commit una posicion mas atrás.

Paso 12 → git reset –hard <id_commit> con este comando movemos la rama en la que estamos al commit anterior y de esa manera podemos recuperar el trabajo. Primero hay que hacer un reflog ya que al modificar 
el wc volvemos a la posicion donde todavia no habiamos creado el commit y por tanto no podemos encontrar su id con un git log normal. Reflog guarda todo el historial de movimientos 
hecho.

Paso → Si que genera un conflicto ya que tengo un archivo git-nuestro.d en la rama main, con un contenido diferente en el mismo sitio en la rama styled.

Paso 19 → Si, por la misma razón que en el caso anterior.

Paso 21 → En este caso no ha causado conflicto como es un merge ff, y por tanto actualiza el archivo en main con el contenido de styled. Esto pasa porque styled esta avanzado a main.

Paso 25-→ git log –graph

Paso 26-→ si, ya que hemos creado la rama en main y al actualizar en title el archivo la rama title va adelantada a main t portanto se puede mover el puntero en una sola direcion 
(no hay divergencia)

Paso 27 → git reset HEAD~1

Paso 28 → git checkout git-nuestro.md (este comando restaura el archivo a al ultima version en que se guardo)

Paso29 → git branch -D  title

Paso 30 → git reflog para encontrar el commit donde hicimos el merge con title y git branch title

Paso 32 → para ir al commit inical git log y git checkout <commit_incial_id>

Paso 33 → como no vemos el final de main, con git reflog buscamos el id del ultimo paso y git checkout de nuevo. Hay que hacer un git branch a main porque estamos Atached HEAD


