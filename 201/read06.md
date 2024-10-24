# ¿Qué hacen los siguientes comandos?

- pwd: Muestra la ruta del directorio de trabajo actual (Print Working Directory).
- ls: Lista los archivos y directorios en el directorio actual (List).
- cd: Cambia el directorio de trabajo actual (Change Directory).
- mkdir: Crea un nuevo directorio (Make Directory).
- touch: Crea un nuevo archivo vacío o actualiza la fecha de modificación de un archivo existente.

## ¿Qué sucede en el siguiente escenario si ingresas estos comandos y argumentos en la línea de comandos?

- cd projects: Cambia al directorio llamado "projects".
- mkdir new-project: Crea un nuevo directorio llamado "new-project" dentro del directorio actual.
- touch new-project/newfile.md: Crea un nuevo archivo vacío llamado "newfile.md" dentro del directorio "new-project".
- cd ..: Regresa al directorio padre del directorio actual (donde estaba antes de entrar a "projects").
- ls projects/new-project: Lista los archivos dentro del directorio "new-project", mostrando newfile.md.

### ¿Qué comando usarías en la terminal para listar todos los archivos, incluidos los archivos ocultos, en un directorio de Linux o macOS?

Usarías el comando:
bash

- (ls -a)
-a: Este parámetro indica que se deben listar todos los archivos, incluyendo los que comienzan con un punto (.), que son considerados ocultos.
