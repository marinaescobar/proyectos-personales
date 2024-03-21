## Guía del correcto flujo de trabajo en un repositorio de Git

### Pasos a seguir

👉🏻 Antes de empezar a trabajar

1. Desde la terminal, accedemos a la ruta de directorios donde se encuentra nuestro repositorio 
    - `cd ruta\del\repositorio`

2. Actualizamos nuestros datos locales con los cambios del repositorio online
    - `git pull`

👏🏻 ¡Ahora ya podemos empezar con nuestro trabajo!<br>

🤔 Pero... ¿Qué pasa si ya hemos terminado y no vamos a hacer más cambios? 

3. Volvemos a actualizar los datos locales con posibles modificaciones que se hayan subido al repositorio online
    - `git pull`

4. Una vez actualizado nuestro repositorio local, subimos todo (incluidos los cambios en los que hemos estado trabajando) al repositorio online
    - `git add -A`
    - `git commit -m "commit_message"`
    - `git push`

5. ¡LISTO!

### Resolución de conflictos: ¿qué hacer?

💀 Morir #JajaNO 

Una vez recuperados del susto, veamos cómo resolverlos:

- Si aún no lo habías hecho, haz `git pull` 
- Si ya hiciste `git pull` y aún así encontraste conflicto, sigue leyendo

**MERGE SUAVE**
- Si los cambios que hemos hecho y los que han hecho otras personas afectan a archivos distintos o a líneas distintas de un mismo archivo, Git nos dará un modo automático de resolver estos conflictos 
- Fíjate en los outputs que te dé Git en la terminal para orientarte 👀 
    - Probablemente tengas que hacer `git config pull.rebase false` e intentar `git pull` de nuevo
- Si ves una pantalla con información acerca del merge automático, haz `ctrl + X` para salir
- Una vez fuera de la pantalla, intenta hacer push de nuevo `git push`

**MERGE DURO**
- Si los cambios que hemos hecho y los que han hecho otras personas afectan a los mismos archivos y en las mismas líneas, Git no podrá resolver los conflictos de forma automática 🥹
- Fíjate en los archivos que Git estará marcando como conflictivos
- Abre los archivos afectados en un editor de texto y resuelve manualmente los conflictos. Podrás:
    - Aceptar aquellos cambios que tú has hecho *(Accept Current Change)*
    - Aceptar los cambios que hay en el repositorio remoto *(Accept Incoming Change)*
    - Modificar manualmente ambos para quedarte con una 3a (y nueva) versión
- Guarda los cambios
- Sube los archivos modificados al repositorio online:
    - `git add -A`
    - `git commit -m "commit_message"`
    -  `git push`


### Otros comandos de interés para Git

- Sincronizar información (de commits, ramas…) desde el repositorio remoto al local, sin cambiar nada de código ni historial. Se puede utilizar siempre que se quiera
    - `git fetch`

- Revisar el estado del repositorio local
    - `git status`

- Distintas maneras de añadir archivos a commitear
    - `git add -A` (añade todos los ficheros que hayan sido modificados)
    - `git add nombre_fichero_concreto` (añade los cambios de un solo fichero)
    - `git add nombre_carpeta/*` (añade los cambios de todos los archivos de un directorio)

- Desestimar un commit anterior porque el archivo contenía fallos o no era correcto
    - `git revert`


