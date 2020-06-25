[`Círculo de estudio`](../Readme.md) > Ejemplo-03
## Herramientas de importación y exportación de datos desde consola

### OBJETIVOS
- Aprender a hacer dumps de bases de datos en MySQL y restaurarlos
- Aprender a hacer dumps de basesde datos en MongoDB y restaurarlos

#### DESARROLLO

Una vez que tenemos intaladas nuestras herramientas de M

1. Abrir la terminal en Linux o MacOS y Git Bash en Windows

1. Localiza los archivos de instalación de tu cliente de Mysql y busca el ejecutable llammado `mysqldump` utilizalo para obtener un archivo dump de mysql.

   ```console
   $ mysqldump -h 127.0.0.1 -u root -p starbucks > starbucks_dump.mysql
   Enter password:
   ```

   Podrás observar que se creo un archivo llamado `startbucks_dump.mysql`, ese archivo contiene código SQL que permite restaurar la información que tenías en tu base de datos a cualquier otra instancia o a esa misma instancia de MySQL.

1. Una vez que tenemos el dump podemos subir esa información a una base de datos en cualquier instancia con el comando `mysql`. Ojo, la base de datos debe estar creada desde antes.

   ```console
   $ mysql -h 127.0.0.1 -u root -p starbucks_copy < starbucks_dump.mysql
   ```

   Y observamos que las tablas que teníamos la primera base ahora también las tenemos en la segunda.

   ```console
   mysql> USE starbucks_copy;
   Reading table information for completion of table and column names
   You can turn off this feature to get a quicker startup with -A

   Database changed
   mysql> SHOW TABLES;
   +--------------------------+
   | Tables_in_starbucks_copy |
   +--------------------------+
   | directory                |
   +--------------------------+
   1 row in set (0.01 sec)

   mysql> 
   ```

1. Tenemos herramientas similares a `mysqldump` para MongoDB. Por ejemplo, con `mongodump` y `mongorestore` podemos guardar colecciones o bases de datos enteras de Mongo.

