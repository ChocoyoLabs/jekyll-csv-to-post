# ekipainteriores-generator

> Solo trabaja con archivos JPG. Para convertir a JPG ver los comandos más abajo.

Genera las publicaciones para el sitio web www.ekipainteriores.com

El primer parámetro es el nombre del archivo que contiene el inventario, el segundo parámetro es el dominio web que se anexará a las url de las fotografías en cada publicación.

## Instalación

    $ npm install ekipainteriores-generator -g

## Ejemplo

    $ ekipainteriores data.csv ekipainteriores.com

## Requerimientos

Requirede del directorio **all_pictures** donde deberá estar almacenadas las fotografías en formato JPG, cada archivo deberá tener el nombre del código del artículo para ser mapeado.

**data.csv** es el inventario de archivos.

## Otros comandos

Convertir archivos PNG a JPG

    $ mogrify -format jpg *.png

Renombrar archivos a minuscula

    $ rename 'y/A-Z/a-z/' *

Renombrar la extensión de arhcivos JPEG a JPG

    $ find . -name "*.jpeg*" -exec rename -v 's/\.jpeg$/\.jpg/i' {} \;
