[`Círculo de estudio`](../Readme.md) > Reto-03
## Herramientas de importación y exportación de datos desde consola

### OBJETIVO
- Aprender a hacer dumps de MySQL
- Aprender a importar datos desde un archivo tipo bson a MongoDB.

#### DESARROLLO


1. Utilizando el ejecutable `mysqldump` genera un archivo *.sql* que contenga la base de datos **classicmodels** que hemos estado utilizando en el curso.

1. Descarga el [archivo bson de la bolsa de valores de NASDAQ](https://dl.dropbox.com/s/p75zp1karqg6nnn/stocks.zip) y utilizando el comando `mongorestore` súbelo a tu cluster de MongoAtlas.