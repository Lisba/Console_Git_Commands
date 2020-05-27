## COMANDOS BÁSICOS DE CÓNSOLA DE GIT:

**git --version** Para leer la version de git instalada.

**git config --global user.name "nombre"** Para configurar usuario.

**git config --global user.email "email@email.com"** Para configurar email.

**cd** entrar a una carpeta.

**cd ..** salir de una carpeta.

**dir** (windows) - **ls** (mac/linux) Ver directorios.

**clear** limpiar la consola.

Click derecho dentro de la carpeta que deseamos sea nuestro repositorio, pulsar el boton git bash ó en mac se arrastra la carpeta a la consola.

**git init** Para crear un repositorio. Sólo se hace una sola vez por proyecto.

**git status** Nos da el status de nuestro repositorio.

**git add .** Para guardar todos los cambios de todos los archivos en nuestro repositorio.

**git commit -m "mensaje descriptivo"** Se utiliza cuando queremos guardar una version de nuestro proyecto.

**git remote add [nombre-remoto] [link]** Vincular repositorio local con repositorio remoto.

**git push -u [nombre-remoto] [rama]** Subir los archivos locales al repositorio remoto. En git al usar push por primera vez se usa "-u" que significa upstring, se usa solo la primera vez que hacemos push a un repositorio creado. Es decirle al sistema que estaremos subiendo todos los bytes necesarios para vincular ambos repositorios, el local y el remoto.

**git push [nombre-remoto]  [rama] -f** Forzar un push si el repo remoto va por delante del repo local. (Esto puede tener efectos destructivos y que se pierdan los commits que van por delante de nosotros).

**git clone [link del repositorio a clonar]** Para clonar un repositorio remoto.

**git commit --amend** Para reescribir el commit anterior (si se olvidó agregar algún archivo o error en el msj del commit).

**git checkout -- [nombre de arichivo]** Revertir código escrito (no funciona despues de un git add).

**git fetch [nombre-remoto]** Para descargar todos los datos del proyecto remoto que no tengo en el local.

**git merge [nombre/rama]** Para mezclar los archivos del repositorio remoto con el repositorio local.

**git pull [nombre-remoto] [rama]** Es un git fetch y git merge juntos.

**git pull [nombre-remoto] [rama] --allow-unrelated-histories**
** Es un git fetch y git merge juntos cuando no permite hacer un git pull comun debido al error: unrelated histories (diferencias en el historial del repo local con el remoto).

**git remote -v** Para ver remotos existentes.

**git remote rename [old] [new]** Cambiar el nombre-remoto del repositorio.

**git remote set-url [name] [new-link]** Cambiar a nuevo GitHub repositorio.

**git remote remove [name]** Eliminar el repositorio remoto.

**git log** Para ver el historial de commits del repositorio.

**git log --oneline** Para ver el historial con cada commit en una sola linea (mas limpio que git log).

**git branch** Para ver las ramas disponibles y en cual estamos.

**git branch [NewBranch-name]** Para crear una nueva rama.

**git branch -d [branch-name]** Para borrar una rama.

**git checkout [branch-name]** Para cambiar de rama.

**git merge [nombreRama]** Para combinar una rama con otra (se debe estar en la master para combinar una rama a la master).

**git checkout [codigo del commit]** (Detached HEAD) Volver al estado de un commit anterior y revisar el codigo o hacer cambios experimentales.

**git branch [nombre rama]  [codigo commit]** Guardar cambios hechos desde un detached HEAD en una rama nueva.

**git reset HEAD [archivo]** para sacar un archivo del área de preparación (no entra en el commit).

**git reflog show** Para mostrar el historial de head antes de hacer un pull.

**git reset --hard** Para deshacer todos los cambios de todos archivos en seguimiento, volviendo al estado del último commit.

**git reset --hard HEAD~1** Para deshacer un commit borrando todos los cambios hechos en el.

**git reset HEAD~1** Para deshacer el commit y volver al estado antes del commit manteniendo las modificaciones hechas en el.

**git reset --keep HEAD@{1}** para volver al ultimo estado de head si algo salió mal (ejemplo: antes de hacer un pull de fork).

Ignorar archivos: Se crea un archivo llamado **.gitignore** y adentro se mencionan todos los archivos y carpetas que deseo que git ignore ( ***.a** ) ( **/folder** ).

Escribir: Si aparece el editor de texto bin en la terminal de git presiono **i** para insertar texto y **:wq** para aplicar el cambio ("w" de write y "q" de quit).

**git add .** == **git add --all**

En caso de que dos personas esten modificando un mismo archivo se genera un conflicto, se combinaran dos archivos, debemos solucionar el conflicto haciendo un git pull para traer los cambios y los veremos en nuestro archivo ligados.
