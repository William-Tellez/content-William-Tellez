---
title: "La Línea de Comando (conocida como: La Terminal)"
subtitle: "Los desarrolladores gastan horas cada día usando la línea de comandos (conocida como: La Terminal). Acepta la realidad y vuélvete más poderoso que nunca."
cover_local: "../../assets/images/4cc6fa0b-2530-4052-aa7e-8dac03788ac3.png"
textColor: "white"
date: "2020-10-19T16:36:31+00:00"
tags: ["línea de comando", "la terminal"]
status: "published"

---

> ☝ Los usuarios de Windows no tienen la misma línea de comando, pero igual deberías aprenderlo, ya que son muy utilizados en los servidores cuando publiques tu página y también en Gitpod, Codespaces, Cloud9, etc. Puedes utilizar [Git SCM](https://git-scm.com/downloads) para probar los comandos.

## ¿Por qué los desarrolladores aman la línea de comando?

Al principio, todos odiaban la línea de comando. Después de años de experiencia, se convirtió en un gusto adquirido.

Pero, ¿por qué les gusta a los desarrolladores? Bueno, la lista es infinita, pero aquí hay algunas razones importantes:

+ Si no dominas la línea de comando, no podrás usar ninguno de estos: GIT, MySQL, Webpack, Node.js, Grunt, Vagrant, Babel, React, Angular, Apache, etc.

+ Como desarrollador, es lo único que necesitas tener disponible. Las computadoras no vienen con Atom, Sublime Text (o cualquier otro IDE de alta calidad). A veces, como en los servidores de producción, no puedes instalar nada (y **el sistema ni siquiera tiene una interfaz visual**), solo la línea de comandos.

+ Es superpoderosa. Puedes hacer mucho más en mucho menos tiempo, por ejemplo: eliminar de forma masiva, cambiar nombres, buscar archivos, editar archivos, etc.
+ Te obliga a usar el teclado. Como no puedes usar el ratón, te hace más rápido, cometes menos errores y el entorno es exactamente el mismo en todas las computadoras.

## ¿Cómo funciona?

La consola es realmente simple: es una pantalla negra que siempre está esperando un *comando*. Después de escribir el comando deseado y de haber presionado la tecla `enter`, la computadora lo ejecuta y muestra algún feedback con el resultado en la pantalla. Una simple interfaz de **Pregunta** <> **Respuesta**.

Pero, ¿qué es un *comando*?

Es algo así como "imprimir", "mostrar", o "eliminar", pero abreviado. Por ejemplo, si quieres decirle a la consola que liste todos los archivos en un directorio en particular, tienes que usar el comando `ls` así:

```bash
ls -l /path/to/directory
```

Todos los comandos tienen tres partes: la **utilidad**, los **marcadores** y los **argumentos**. La utilidad siempre es lo primero. Las otras dos partes tienen reglas diferentes y, dependiendo del comando que estés utilizando, es posible que no tengas que usar ningún marcador o argumento.

En este caso particular, usamos el "marcador" `-l` para especificar que queremos una versión "larga" de la lista de archivos (con más detalles).

Lo último que tenemos que agregar es el "argumento". En este caso, el "argumento" será la ruta del directorio del cual queremos listar los archivos.

## ¿Qué puedes hacer en la terminal?

Tu computadora tiene archivos, directorios y aplicaciones. Tu línea de comando es capaz de lidiar con los tres. Usa comandos para moverte dentro de los archivos y directorios (como el comando `cd` que es el acrónimo de *change directory*). Cada aplicación que instales viene con un conjunto de comandos que están disponibles a partir del momento en que instales la aplicación (como el comando GIT).

## Así es como se ve el sistema de archivos en una interfaz visual versus la terminal:

![Interfaz Visual vs La Terminal](https://github.com/breatheco-de/content/blob/master/src/assets/images/182ea93c-9d7d-4c8d-8153-9c1756d8cd1f.png?raw=true)

Hay 4 cosas importantes que notar aquí:

+ Puedes usar un punto `.` para referirte a todos los archivos y carpetas en la jerarquía.
+ También puedes usar dos puntos `..` para referirte al directorio padre.
+ Puedes usar la barra diagonal `/` para navegar más hacia abajo en la jerarquía de directorios.
+ Archivos ocultos: Por lo general, un archivo tiene un nombre y una extensión *(filename.extension)*. Si un archivo no tiene nombre y solo una extensión, estará, por defecto, oculto en la interfaz visual.

## Comandos para trabajar con el sistema de archivos

Aquí hay una pequeña selección de los comandos más utilizados por un desarrollador de software.

### El comando ls

**El comando de lista**

El comando `ls` se usa para listar todos los archivos y directorios que forman la posición actual.

```bash
ls -l ./applications
# Muestra los archivos y carpetas dentro de "applications"
# El -l es para recibir una información más detallada sobre los archivos
```

### El comando cd

**El comando para cambiar de directorio**

Navega entre dos directorios diferentes.

```bash
cd /path/to/directory
```

### El comando mv

**El comando mover**

Mueve un archivo a otra carpeta o directorio, como por ejemplo arrastrar un archivo ubicado en el escritorio de una PC a una carpeta almacenada dentro de la carpeta "Documentos".

```bash
mv /path/to/file.txt /math/to/destination/file.txt
```

### El comando rm

**El comando eliminar**

Borra archivos (no directorios).

```bash
rm file1.txt file2.txt file3.txt file4.txt
# Elimina estos cuatro archivos

rm -r dbstore/
# Elimina todos los archivos y subdirectorios recursivamente dentro del directorio "dbstore"
```

### El comando mkdir

**El comando crear directorio**

Crea un nuevo directorio. Al igual que para crear un nuevo directorio en un escritorio de PC o Mac, el comando `mkdir` crea nuevos directorios en un entorno Linux.

```bash
mkdir newdirectoryname
# Crear newdirectoryname en el directorio actual

mkdir path/of/new/newdirectoryname 
# Crear newdirectoryname dentro de /path/of/new/
```

### El comando rmdir

**El comando eliminar directorio**

Elimina un directorio (no archivos).

```bash
rmdir mydirectory
# Eliminar mydirectory si está en el directorio actual 

rmdir path/of/targetdirectory/mydirectory
# Eliminar mydirectory de "targetdirectory" 
```

> ☝ Solo eliminará los directorios vacíos, para vaciar todos los archivos del directorio usa el comando `rm`. Pro-tip: puedes usar `rm *` para borrar todos los archivos dentro de un directorio simultáneamente; utilízalo con precaución.

### El comando cp

**El comando copiar archivo**

No confundas este comando con la funcionalidad de copiar del portapapeles, no tiene nada que ver con eso.

`cp` Copiará un archivo completo y creará uno nuevo con el nombre que decidas que deba tener.

```bash
cp path/to/file.txt path/to/new/file_copy.txt
# Copia "file.txt" y crea un nuevo "file_copy.txt" con el mismo contenido
```

### El comando find

**El comando encontrar**

Encuentra un archivo en el directorio dado y con las especificaciones dadas.

```bash
find / -name game
# Encuentra todos los archivos que contengan el nombre exacto "game" que se encuentran dentro de la carpeta raíz.

find . -name *.mp3
# Encuentra todos los archivos que contengan la extensión "mp3" dentro del directorio actual y en el de su padre.
```

## Consejos y trucos

Esto te ayudará a ahorrar tiempo y a cometer menos errores al escribir:

+ Para cancelar un comando que se está ejecutando, presiona `ctrl + c`.
+ Para completar automáticamente el nombre de un archivo o carpeta, usa la tecla `tab`.
+ Para repetir cualquier comando que hayas usado en el pasado, usa la flecha arriba `↑` y te mostrará cada comando, uno por uno.
+ Para ir a la carpeta principal del usuario, usa la tecla `~`, así: `cd ~`.
+ Usa el comando `clear` para "limpiar" la consola actual (es solo un desplazamiento, pero muy útil).

## Editando archivos en la terminal

Esta es una de las cosas que no puedes evitar hacer en la terminal. Como desarrollador, tendrás que editar archivos en la terminal con más frecuencia de lo que crees. Por eso es mejor que estés preparado para usar la [Aplicación VIM o la Aplicación Nano.](https://askubuntu.com/questions/726669/difference-between-nano-and-vim) Hablaremos sobre Nano y sus comandos (sí, aquí el editor de texto se abre dentro de la línea de comandos y se ejecuta usando comandos).

### El comando nano

**No es realmente un comando, sino una aplicación de edición de texto con el nombre de "Nano".**

Cuando trabajes con la línea de comandos, a veces tendrás que abrir un archivo para revisarlo e incluso para cambiarlo. Para eso, usamos el comando `nano`. Nano básicamente abre un editor de texto dentro de la línea de comando.

```bash
nano path/to/the/textfile.txt
# Abre un editor de texto para comenzar a editar el contenido de textfile.txt
# Si textfile.txt no existe ¡lo creará!
```

Cuando nano se abra, verás una barra superior con la versión actual de la aplicación nano, el nombre del archivo que se está editando, y un estado indicándote si los archivos fueron modificados o no.

En la parte inferior verás los comandos más utilizados para usar nano, tales como: exit, where is, get help, etc.

![the command line the terminal](https://github.com/breatheco-de/content/blob/master/src/assets/images/6128e9f7-b460-4b10-80e4-34057b7d4df9.png?raw=true)

> ☝ Este sitio web tiene un montón de pequeños mini desafíos para ayudarte a practicar la línea de comandos: https://cmdchallenge.com/
