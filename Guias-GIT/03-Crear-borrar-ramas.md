## Guía para la creación y eliminación de ramas en Git

### Creación de una rama

1. Desde la terminal, accedemos a la ruta de directorios donde se encuentra nuestro repositorio 
    - `cd ruta\del\repositorio`

2. Existen varios métodos para crear una rama, veámoslos:

    - Crear y nombrar una nueva rama local:
        -  `git branch nombre_rama_especifica`

    - Crear, nombrar y movernos a una nueva rama local:
        -  `git checkout -b nombre_rama_especifica`

    *¿Cuál es la diferencia entre ambos métodos?* 
    <br>💡 Mientras que el primero sólo crea la rama (seguiremos estando en **main**), el segundo la crea y nos mueve a ella (pasaremos a estar en **nombre_rama_especifica**)

3. Después de haber trabajado en la rama que hemos creado, **la primera vez que hagamos push** de nuestros commits utilizaremos:
    - `git push -u origin nombre_rama_especifica`

    *¿Por qué sólo la primera vez?* 
    <br>💡 Dado que en el paso anterior hemos creado la rama de forma local, la primera vez que hacemos push tenemos que crearle su equivalente remoto

### Eliminación de una rama

1. Desde la terminal, accedemos a la ruta de directorios donde se encuentra nuestro repositorio 
    - `cd ruta\del\repositorio`

2. Nos movemos a la rama que queremos eliminar
    - `git checkout nombre_rama_especifica`

3. Comprobamos que no haya cambios pendientes de unificar
    - `git status`
    <br>👉🏻 Si los hubiera, consulta la guía *04-Trabajo-en-ramas.md* para ayudarte a unificarlos

4. Volvemos a la rama **main**
    - `git checkout main`

5. Eliminamos la rama local
    - `git branch -d nombre_rama_especifica`

6. Eliminamos la rama remota
    - `git push origin --delete nombre_rama_especifica`