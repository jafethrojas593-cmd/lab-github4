# lab-github4
testing alexia
organizacion de archivos 
testing de dylan
organizacion de archivos
testing jafeth
test fallo 
# Explicacion
Cuando trabajamos en un proyecto y modificamos algún archivo, esos cambios no se guardan automáticamente en el repositorio. Por eso existe git add, que sirve para indicarle a Git qué archivos queremos incluir en el próximo registro de cambios. Es como seleccionar qué modificaciones formarán parte de la siguiente versión. Por ejemplo, si editamos index.html, usamos git add index.html. Y si queremos preparar todos los archivos modificados, usamos git add ..

Después viene git commit -m, que es como capturar una “fotografía” del estado del proyecto. Un commit registra formalmente los cambios que realizamos, acompañado de un mensaje que explique qué se hizo o el motivo. Ese comentario ayuda a mantener un historial claro. El parámetro -m significa “message”. Por ejemplo:
git commit -m "Corrijo el error del formulario".

Luego está git push, que se utiliza para enviar los commits al repositorio remoto, como GitHub. Básicamente es subir nuestro trabajo de la computadora local a la nube. En algunos casos es necesario usar un push forzado (git push -f), normalmente cuando los cambios locales no coinciden con los del repositorio remoto. El push forzado sustituye la versión remota con la local, por lo que debe usarse con precaución porque podría borrar el trabajo de otros.

Por su parte, git pull hace lo contrario: trae a nuestra máquina los cambios que se encuentran en el repositorio remoto. Es fundamental cuando se trabaja en equipo, ya que garantiza que estemos trabajando con la versión más actual del proyecto.

También existe git rebase, que sirve para reorganizar o reaplicar commits sobre otra base. En lugar de hacer merges que a veces generan un historial complicado, el rebase acomoda los cambios de manera que parezca que se hicieron en secuencia limpia. Es útil para mantener un historial más ordenado, especialmente cuando se trabaja con varias ramas.

Un caso especial es git rebase -i HEAD~x, donde “x” representa cuántos commits hacia atrás queremos revisar. El -i significa “interactivo”, lo que nos permite editar, unir, renombrar o incluso eliminar commits anteriores. Por ejemplo, git rebase -i HEAD~3 permite modificar los últimos tres commits antes de compartirlos. Es como poder ajustar la historia del proyecto antes de publicarla.

El comando git status nos da un resumen de la situación actual: qué archivos han cambiado, cuáles están listos para commit y en qué rama estamos trabajando.

Con git log podemos ver el historial completo de commits: quién hizo cada cambio, cuándo lo hizo y el mensaje que dejó. Esto ayuda a entender cómo ha evolucionado el proyecto y facilita encontrar errores del pasado.

El comando git diff se utiliza para ver las diferencias precisas entre versiones o entre lo que tenemos en el área de trabajo y lo ya registrado. Es como comparar dos textos y resaltar las líneas que cambiaron.

git branch permite consultar todas las ramas del proyecto o crear una nueva. Una rama funciona como una línea de desarrollo independiente de la principal. Por ejemplo, git branch nueva-rama crea una nueva, y ejecutar solo git branch muestra el listado de todas las ramas.

Si queremos borrar una rama local, usamos git branch -D. La -D significa “delete” y fuerza el borrado completo de la rama, por lo que debe usarse con cuidado.

Con git checkout podemos movernos entre ramas o versiones anteriores del proyecto. Es como cambiar de una línea de trabajo a otra. Por ejemplo, git checkout nombre-de-rama cambia a esa rama. También se puede usar para restaurar un archivo a una versión anterior.

Finalmente, git commit --amend sirve para modificar el último commit. Si se nos olvidó incluir un archivo o queremos ajustar el mensaje, este comando reescribe ese último registro. Es como editar la última foto antes de archivarla.
Si solo deseamos actualizar el contenido del commit sin cambiar el mensaje, se usa git commit --amend --no-edit. Esto reemplaza los cambios del commit anterior, pero deja el texto del mensaje intacto. Es ideal para pequeñas correcciones de último momento.