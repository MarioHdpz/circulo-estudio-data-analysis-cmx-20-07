[`Círculo de estudio`](../Readme.md) > Ejemplo-02
## Instalación y ejecución de software desde terminal

### OBJETIVOS
- Aprender a instalar software desde terminal
- Aprender sobre manejadores de paquetes y aplicaciones
- Entender cómo funciona la instalación y dónde están los ejecutables

### DESARROLLO
1. Abrir la terminal en Linux o MacOS y Git Bash en Windows

1. Reconoce el software que utilizarás como gestor de paquetes o aplicaciones. En el caso de Linux el manejador o gestor que usamos por defecto es `apt` (Advanced Packaging Tool), y debemos procurar mantenerlo actualizado con el comando `apt-get update`.

   ```console
   $ sudo apt-get update 
   [sudo] password for mario: 
   Get:1 http://dl.google.com/linux/chrome/deb stable InRelease [1 811 B]
   Hit:2 http://mx.archive.ubuntu.com/ubuntu focal InRelease
   Fetched 1 272 kB in 4s (317 kB/s)             
   Reading package lists... Done
   ```

   En el caso de MacOS el gestor o manejador de paquetes que se recomienda utilizar es [Homebrew](https://brew.sh/)

1. Con el gestor de paquetes puedes instalar software de manera muy sencilla, por ejemplo, puedes usarlo para instalar el cliente de MySQL. 

   ```console
   $ sudo apt-get install mysql-client-core-8.0
   Reading package lists... Done
   Building dependency tree       
   Reading state information... Done
   The following NEW packages will be installed:
   mysql-client-core-8.0
   0 upgraded, 1 newly installed, 0 to remove and 31 not upgraded.
   Need to get 4 196 kB of archives.
   After this operation, 64.7 MB of additional disk space will be used.
   Get:1 http://mx.archive.ubuntu.com/ubuntu focal-updates/main amd64 mysql-client-core-8.0 amd64 8.0.20-0ubuntu0.20.04.1 [4 196 kB]
   Fetched 4 196 kB in 2s (1 757 kB/s)                    
   Selecting previously unselected package mysql-client-core-8.0.
   (Reading database ... 203549 files and directories currently installed.)
   Preparing to unpack .../mysql-client-core-8.0_8.0.20-0ubuntu0.20.04.1_amd64.deb ...
   Unpacking mysql-client-core-8.0 (8.0.20-0ubuntu0.20.04.1) ...
   Setting up mysql-client-core-8.0 (8.0.20-0ubuntu0.20.04.1) ...
   Processing triggers for man-db (2.9.1-1) ...
   ```

   En el caso de MacOS puedes hacerlo con Homebrew

   ```console
   $ brew install mongodb-community@4.2
   ```

1. Para revisar que tu programa haya sido instalado puedes utilizar el parámetro `--version`

   ```console
   $ mysql --version
   mysql  Ver 8.0.20-0ubuntu0.20.04.1 for Linux on x86_64 ((Ubuntu))
   ```

   Además puedes ver en qué lugar se instaló tu paquete usando el comando `which`

   ```console
   $ which mysql
   /usr/bin/mysql
   ```

   Esto significa que tu gestor lo que hizo fue copiar los archivos de instalación a la carpeta `/usr/bin/`, en caso de `which` no funcione puedes navegar hasta tu carpeta de instalaciones y correrlo desde ahí

   __Nota__ Para que which funcione se debe de agregar la ruta de instalación al `PATH` de la terminal, pero esto varia para cada sistema operativo. Aunque en la mayoría de los casos se hace modificando el archivo `.bashrc` que esta en la ruta principal de tu usuario.

1. Una vez que tengamos el cliente de mysql instalado podemos usarlo para conectarnos a una base de datos desde consola.

   ```console
   $ mysql -h 127.0.0.1 -u root -p
   Enter password: 
   Welcome to the MySQL monitor.  Commands end with ; or \g.
   Your MySQL connection id is 1504
   Server version: 8.0.13 MySQL Community Server - GPL

   Copyright (c) 2000, 2020, Oracle and/or its affiliates. All rights reserved.

   Oracle is a registered trademark of Oracle Corporation and/or its
   affiliates. Other names may be trademarks of their respective
   owners.

   Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

   mysql> 
   ```

__Misión cumplida__