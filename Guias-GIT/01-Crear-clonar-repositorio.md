## Guía para crear y clonar un repositorio de Git

### Creación de un repositorio

1. Iniciamos sesión en nuestra cuenta de GitHub en el navegador web

2. Hacemos clic en el signo **(+)** de la esquina superior derecha y seleccionamos **"New repository"** de entre las opciones disponibles

3. Ya en la nueva pantalla, ingresamos la información del repositorio:
    - Nombre del Repositorio: Introducimos un nombre descriptivo para nuestro repositorio.

    - Descripción (opcional): Proporcionamos una breve descripción que explique el propósito del repositorio.

    - Visibilidad: Podemos elegir entre "Public" (público) o "Private" (privado). Los repositorios públicos son visibles para todos, mientras que los privados solo son accesibles por los colaboradores designados.

    - Inicializar este repositorio con: Opcionalmente, podemos seleccionar una plantilla de licencia, un archivo README o un archivo .gitignore que sea relevante para nuestro proyecto.

4. Tras completar la información requerida, hacemos clic en el botón **"Create repository"** 

### Configuración adicional del repositorio (añadir colaboradores)

1. En la página principal del repositorio, hacemos clic en la pestaña **"Settings"**

2. En el menú lateral izquierdo, seleccionamos **"Collaborators"**

3. Ingresamos el nombre de usuario de las personas que queremos añadir como colaboradores y hacemos clic en **"Add collaborator"**

### Clonación de un repositorio

1. Desde la terminal, accedemos a la ruta de directorios donde desearemos clonar el repositorio 
    - `cd ruta\donde\ubicar\el\repositorio`

2. Clonamos el repositorio:
    -  `git clone url_repositorio`

    *¿Dónde puedo encontrar esa url?* 
    <br>💡 Podemos copiar la URL de clonación que nos proporcione la propia la plataforma (GitHub, GitLab...) después de haber creado el repositorio