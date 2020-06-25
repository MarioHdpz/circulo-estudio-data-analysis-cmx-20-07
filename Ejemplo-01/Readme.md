[`Círculo de estudio`](../Readme.md) > Ejemplo-01
## Terminal y comandos para navegar por el sistema de archivos

### OBJETIVO
- Conocer la terminal
- Conocer y ejecutar comandos para navegar por el sistema de archivos
- Adquirir la habilidad en el uso de la terminal

#### DESARROLLO
1. Abrir la terminal (Linux y Mac) o Git Bash (Windows)

1. Obtener la ruta (o path) de la carpeta actual, escribe el comando `pwd` y presiona ENTER:
   ```console
   $ pwd
   /home/mario
   ```
   Todo lo que aparece desde el inicio de la línea hasta el signo de $ es lo que se conoce como la señal o prompt del sistema operativo, el símbolo de $ no lo tienes que teclear, sólo indica que lo que tu vayas a teclear será después de ese símbolo.
   El comando en este caso es `pwd` y para ejecutarlo has presionado la tecla __ENTER__.
   El resultado se muestra en la línea siguiente y es `/home/mario`.

   El comando `pwd` te permite siempre conocer la carpeta de trabajo en la que te encuentras.

1. Obtener la lista de elementos de la carpeta actual, escribe el comando `ls` y presiona ENTER:
   ```console
   $ ls
    bin                           Documentos      Música         Escritorio      Sesion08                      Notas.md        Vídeos
    DesarrolloPython              Imágenes        Plantillas     miniconda3      Público                       Descargas       CursoBD     repos
   $
   ```
   En Linux y MacOS el resultado es como el mostrado, en Windows la lista podrá aparecer en una sola columna.

1. El comando `ls` se le pueden agregar opciones para que proporcione más información de los elementos, así que una alternativa es usar la opción `-l` que mostrará permisos, usuario y grupo propietarios, tamaño, fecha y nombre.
   ```console
   $ ls -l
   drwxrwxr-x  2 mario mario     4096 oct 29 14:47  bin/
   drwxr-xr-x  8 mario mario     4096 nov 26 12:08  Descargas/
   drwxr-xr-x  5 mario mario     4096 nov 21 15:52  Documentos/
   drwxr-xr-x  2 mario mario     4096 nov 23 09:25  Escritorio/
   drwxr-xr-x  2 mario mario     4096 nov 25 19:54  Imágenes/
   drwxrwxr-x 15 mario mario     4096 nov 11 10:42  miniconda3/
   drwxr-xr-x  2 mario mario     4096 oct 20 04:43  Música/
   -rwxr-xr-x  1 mario mario      390 nov  9 13:39  my_script.sh*
   -rw-rw-r--  1 mario mario      160 nov 23 09:29  Notas.md
   drwxr-xr-x  2 mario mario     4096 oct 20 04:43  Plantillas/
   drwxrwxr-x  6 mario mario     4096 nov 19 05:18  repos/
   drwxr-xr-x  3 mario mario     4096 oct 27 03:15  Vídeos/
   $
   ```
   De aquí en adelante puedes elegir entre usar `ls` o `ls -l` según te convenga.

1. Cambiar de carpeta se realiza con el comando `cd CursoBD`
   ```console
   $ cd CursoBD
   CursoBD $
   ```
   Es posible que al cambiar de carpeta, en el prompt se muestre el nombre de la carpeta en la que te encuentras o posiblemente no (CursoBD en este caso), eso varía de sistema a sistema, así que no aparece no te preocupes, siempre puedes ocupar el comando `pwd`.

1. Examinar el contenido de la carpeta actual con el comando `ls`
   ```console
   CursoBD $ ls
   ```
   Al estar la carpeta vacía se muestra una nueva línea con el prompt sin indicar mensaje alguno, tranquilx, todo está bien.

   También podemors ver cómo la ruta ha cambiado con el comando `pwd`

   ```console
   CursoBD $ pwd
   /home/mario/CursoDB
   ```


1. Para regresar a una carpeta anterior se hace uso del comando `cd ..`
   ```console
   CursoBD $ cd ..
   $
   ```

__Misión cumplida__
