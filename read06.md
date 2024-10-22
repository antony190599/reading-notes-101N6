**💻 Comandos de la línea de comandos en Unix (Linux o macOS)**

**¿Qué hacen los siguientes comandos?**

- pwd:
Muestra la ruta del directorio de trabajo actual. Es útil para saber en qué parte del sistema de archivos te encuentras.

- ls:
Lista los archivos y directorios dentro del directorio actual. Puede utilizarse con opciones adicionales, como -l para detalles y -a para incluir archivos ocultos.

- cd:
Significa "change directory" (cambiar de directorio). Lo utilizas para moverte entre directorios en el sistema de archivos.

- mkdir:
Crea un nuevo directorio en la ubicación actual o en la ruta especificada.

- touch:
Crea un archivo vacío o actualiza la fecha de modificación de un archivo existente.

**🔄 Escenario de uso práctico**

**Imagina que ejecutas los siguientes comandos en la terminal:**

cd projects:
Cambia al directorio llamado projects, suponiendo que existe en la ubicación actual.

mkdir new-project:
Crea un nuevo directorio llamado new-project dentro del directorio projects.

touch new-project/newfile.md:
Crea un archivo vacío llamado newfile.md dentro de new-project. Si el archivo ya existe, se actualiza su fecha de modificación.

cd:
Retrocede un nivel en la estructura de directorios, volviendo al directorio padre.

ls projects/new-project:
Lista el contenido del directorio new-project, donde ahora aparece el archivo newfile.md.

**🛠️ ¿Cómo listar todos los archivos, incluidos los ocultos, en un directorio de Linux o macOS?**
**Para listar todos los archivos, incluidos los archivos ocultos, puedes usar el siguiente comando:**

- ls -a
  
Desglose del comando:

- ls: Lista los archivos y directorios en el directorio actual.
  
-a: Opción que incluye archivos ocultos (aquellos cuyo nombre comienza con un punto .).
