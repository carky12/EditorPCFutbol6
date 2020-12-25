# EDITOR PC FÚTBOL 6.0

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/Fondo.bmp) 

#### Creado por carky12

## Breve Descripción

En este documento se exponen las explicaciones necesarias para poder utilizar el editor de pc fútbol 6.0. 

El editor es válido para versiones 
- PC FÚTBOL 6.0
- PC FÚTBOL 6.0 EXTENSION 1
- PC FÚTBOL 6.0 EXTENSION 2
- PC PREMIER
- PC CALCIO
- PC APERTURA

Opcionalmente se puden generar archivos de equipo DBC para versiones 5.0

El manual completo (con capturas y en PDF) está en este enlace: [Manual Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Manuales/Manual%20Editor%20PCF%C3%BAtbol%206.pdf)

Podéis ver los videos del Editor funcionando en los siguientes enlaces de YouTube:

[Edición de competiciones](https://www.youtube.com/watch?v=SMxl0EtCkTs&feature=youtu.be&ab_channel=CarlosGonz%C3%A1lez)

[Generación de archivos DBC](https://www.youtube.com/watch?v=ChxB0d5TN6Y&feature=youtu.be&ab_channel=CarlosGonz%C3%A1lez)

[Actualzación masiva desde una web](https://www.youtube.com/watch?v=IAcNQdtkJOE&feature=youtu.be&ab_channel=CarlosGonz%C3%A1lez)


## Dedicatoria

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/dedicatoria1.png) 
![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/dedicatoria4.png) 

Quisiera dedicar este proyecto a todo el mundo que durante este año ha perdido a alguien. Ha sido un año muy duro para todos, en el que hemos perdido, y no solo hemos perdido cercanos, hemos perdido leyendas, que de una manera u otra han marcado a una generación entera (mi generación).

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/dedicatoria6.png) 
![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/dedicatoria5.png) 
![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/dedicatoria7.jpg) 

No voy a nombrar a ninguno de los grandes que se han ido en este 2020, por que sería injusto con respecto a los que se han ido y no son nombrados. Sin más mucha fuerza todos y ánimo para este 2021!

## Índice

- [Introducción](#introducción).
- [Versiones del juego aceptadas por el editor](#versiones-del-juego-aceptadas-por-el-editor)
- [Rutas que utiliza el editor](#rutas-que-utiliza-el-editor)
- [Cargar archivo de equipos](#cargar-archivo-de-equipos)
- [Edición de Equipos](#edición-de-equipos)
- [Edición de Jugadores](#edición-de-jugadores)
- [Abrir Archivo DBC (Formato 5.0 y 6.0)](#abrir-archivo-dbc)
- [Importar información desde la WEB](#importar-información-desde-la-web)
- [Edición de competiciones](#edición-de-competiciones)
- [Edición del Calendario](#edición-del-calendario)
- [Selección de Escudos](#selección-de-escudos)
- [Selección de Fotos de jugadores](#selección-de-fotos-de-jugadores)
- [Actualización masiva desde una web](#actualización-masiva-desde-una-web)
- [Utilidades](#utilidades)
- [Logs](#logs)
- [Edición hexadecimal de archivos DBC](#edición-hexadecimal-de-archivos-dbc)

## Introducción

En este documento se explica el funcionamiento del editor de PC Fútbol 6. También se explicarán
conceptos básicos en la edición del juego (jugadores, equipos, competiciones, etc...).

El editor se basa en generar archivos DBC para colocar en la carpeta DBDAT. En esta carpeta se
generará una carpeta con el nombre del archivo de equipos PKF correspondiente a la versión
del juego – Ejemplo para PC Premier el directorio donde dejar los archivos DBC será “PC
PREMIER6\DBDAT\EQ030022\”. En este directorio es donde se pondrán los ficheros DBC
generados con el editor. Dentro de DBDAT también tendrán que existir los directorios para las
fotos de los jugadores (“DBDAT\MINIFOTOS”) y escudos de los equipos (“DBDAT\MINIESC”,
“DBDAT\NANOESC”) que se generen con el editor.

## Versiones del juego aceptadas por el editor

El editor funciona para las siguientes versiones del juego:

- PC Fútbol 6.0: Archivo de equipos EQ022022.PKF. Tamaño del manager 2556 KB.
- PC Fútbol 6.0 Extensión 1: Archivo de equipos EQ022022.PKF. Tamaño del manager 2569 KB.
- PC Fútbol 6.0 Extensión 2: Archivo de equipos EQPCPLUS.PKF. Tamaño del manager 2486 KB.
- PC Premier 6.0: Archivo de equipos EQ030022.PKF. Tamaño del manager 2771 KB.
- PC Calcio 6.0: Archivo de equipos EQ036022.PKF. Tamaño del manager 2513 KB.
- PC Apertura 6.0: Archivo de equipos EQ003003.PKF. Tamaño del manager 2397 KB.

En estas versiones se pueden editar lo siguiente:

Generación de equipos
- Edición de equipos a partir de un archivo DBC
- Edición de jugadores contenidos en un archivo DBC
- Edición de las competiciones del archivo manager.exe
- Edición del calendario.
- Seleccionar fotos para jugadores.
- Seleccionar escudos para equipos.
- Actualización automática de equipos desde una página de internet.

El editor permite guardar archivos DBC con el formato para cualquier versión 5.0 del juego, sin
embargo, por ahora, no se pueden editar ni el calendario ni las competiciones de estas
versiones.

## Rutas que utiliza el editor

- “\Archivos Originales”: Directorio que contiene los archivos de equipos y managers originales para cada versión del juego soportada por el editor. Es recomendable NO TOCAR nada en este directorio. Por ejemplo, los archivos manager.exe se utilizan para comparar con el que carguemos en el editor y así saber las posiciones que hay que tocar para cambiar el calendario.
- “\Actualización”: Directorio en el que se generan los ficheros para la realización de la actualización de forma masiva desde la web. Se generará un directorio por cada país que tenga liga en el juego.
- “\EquiposDBC”: Directorio en el que se guardarán los archivos DBC generados con el editor.
- “\Imagenes”: Directorio en el que se guardarán los escudos y fotos de jugadores generadas con el editor.
- “\Logs”: Directorio en el que se irán guardando los logs de cada sesión del editor.
- “\Manager”: Directorio en el que se guardarán los archivos manager generados por el editor.

## Cargar archivo de equipos

Lo primero que hay que hacer al entrar al editor es cargar el archivo PKF de equipos, correspondiente a la versión que vayamos a actualizar. Esto es imprescindible para que se puedan generar los punteros, tanto de equipos como de jugadores, de forma automática. El editor asigna punteros de 50 en 50 a cada equipo, además de leer los punteros originales de cada equipo del archivo PKF.

Una vez cargado el fichero PKF se habilitarán los menús para comenzar la edición.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor1.png) 

## Edición de Equipos

Se podrá consultar los equipos originales del archivo PKF, editar un equipo desde un fichero DBC,
o generar un fichero DBC nuevo.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor2.png) 

### Consulta de equipos

Desde esta pantalla podremos consultar los equipos contenidos en el archivo PKF cargado al
inicio. Esto nos puede ser útil para conocer su puntero (tanto en formato decimal como en
formato hexadecimal).

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor3.png) 

Desde esta pantalla podremos realizar la búsqueda de equipos por nombre, puntero (si es que
conocemos su puntero) o por país.

### Nuevo archivo DBC

Desde esta pantalla podremos generar un archivo DBC de múltiples formas. Podremos cargar
un archivo DBC existente y cambiar lo que necesitemos, podremos generar un archivo DBC
totalmente desde cero y también podremos importar datos desde una web.

#### Pestaña de Equipo

Desde aquí podremos definir todos los datos generales de un equipo. Los campos marcados en
azul oscuro son obligatorios, los demás los guarda el propio editor de forma predeterminada.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor4.png) 

Para guardar el fichero tendremos las siguientes opciones.

1: Generar EQ96XXXX.DBC: Si marcamos esta opción el archivo se generará con el nombre
“EQ96” en lugar de “EQ97”.

2: Usar nombre de equipo para generar el archivo DBC: Si marcamos esta opción se guardará el
archivo usando el nombre real del equipo en lugar de “EQ97XXXX.DBC”

3: Usar formato 5.0 al guardar el archivo: Si marcamos esta opción se guardará un archivo DBC
respetando el formato de las versiones PCF 5.0.

En la parte superior podemos ver los campos de los punteros. Estos campos no son editables. Si
están vacíos se guardará el fichero DBC con el nombre EQ970000.DBC, y los para los punteros
de los jugadores se utilizarán de forma consecutiva desde el número 1.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor5.png) 

Si pulsamos en el botón con los “...” se mostrará una ventana en la que podremos seleccionar
un equipo. En esta ventana se muestran los equipos originales del archivo PKF cargado al inicio.
En dicha ventana podremos buscar un equipo por nombre.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor6.png) 

Al seleccionar un equipo se mostrará:

1: el puntero decimal

2: el puntero hexadecimal

3: el nombre del equipo y el nombre del fichero DBC que resultará al guardar

4: los punteros de jugadores que se utilizarán. Se reservan 49 punteros para cada equipo,
empezando en el primer equipo (Barcelona) que se reservan los punteros del 1 al 50, para el
segundo equipo (Deportivo) del 51 al 100, y así hasta el último equipo.

**IMPORTANTE** : Al cargar un fichero, se intenta buscar el puntero entre la lista de equipos
originales cargados (archivo PKF). Si por lo que fuese no se encuentra el puntero y se guarda de
nuevo el fichero DBC se sobrescribirán los punteros de jugadores. Ejemplo: Si tienes un fichero
EQ970004.DBC al cargarlo se realizará la búsqueda de cuál es el equipo que tiene e puntero
“0004” decimal. Resultará el Real Madrid, con lo que se rellenarán los campos correspondientes
y los punteros de jugadores serán los mismos, es decir, del 151 al 200. Si el archivo que cargamos
se llama EQ979999.DBC, no se encontrará ningún equipo con puntero decimal “9999” por lo que
los punteros de jugadores que se utilizarán al guardar este fichero serán del 1 al 50.

#### Pestaña de Tácticas

Desde aquí podremos editar la táctica que utilizará el equipo. Por defecto, si no seleccionamos
nada se guarda lo que se muestra en la captura.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor7.png) 

#### Pestaña Plantilla

Desde esta pestaña podremos consultar la plantilla de jugadores que hay en el archivo DBC
además de crear un jugador nuevo.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor8.png) 

La lista de jugadores se ordenará por demarcación, siguiendo este orden: primero los porteros,
después los defensas, los medios y por último los delanteros. Pulsando el botón “Nuevo”
accederemos a la pantalla de creación de jugadores.

En la lista podremos consultar el nombre corto del jugador, el nombre largo del jugador, la media
global, la demarcación, podremos acceder a la edición de sus datos y borrarlo de la plantilla.

**IMPORTANTE** : Debido a la ordenación de los jugadores en la lista si tenemos un equipo con 25
jugadores con sus respectivos punteros, y añadimos un portero, se recalcularán los punteros de
los 26 jugadores (ya que se ha incrustado un jugador en medio de otros ya existentes). Hay que
tener esto en cuenta por si tenemos fotos de jugadores asociados a punteros de equipos ya
guardados. Por eso lo mejor es dejar la edición de las fotos para cuando se tengan todos los
equipos perfectamente actualizados.

### Acciones que se pueden realizar

Desde la pantalla de edición de equipos se pueden realizar las siguientes acciones

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor9.png) 

1: Editar las características de un jugador de la plantilla. Al pulsar este botón se accede a la
pantalla de edición de jugador.

2: Borrar un jugador de la plantilla.

3: Guardar un archivo DBC.

4: Cargar un archivo DBC (con formato 6.0). Se muestra un cuadro de diálogo en el que se podrá
seleccionar un fichero DBC.

5: Cargar n archivo DBC (con formato 5.0). Se muestra un cuadro de diálogo en el que se podrá
seleccionar un fichero DBC.

6: Importar información desde la web. Al pulsar este botón se accede a la pantalla de importar
información.

7: Seleccionar una imagen de escudo para el equipo. Se muestra un cuadro de diálogo en el que
se podrá seleccionar un fichero DBC.

8: Añadir un nuevo jugador a la plantilla. Al pulsar este botón se accede a la pantalla de edición
de jugador.

Ejemplo: Al cargar el fichero “EQ970004.DBC” se busca en los equipos originales y se encuentra
al Real Madrid:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor10.png) 

De esta forma nos desentendemos de la gestión de los punteros, simplemente hay que ser un
poco organizados con la edición y el editor se encarga del resto.

## Edición de Jugadores

Podremos editar cualquier jugador contenido en un fichero DBC. Para editar a un jugador hay
que cargar primero el archivo DBC y desde la pestaña plantilla presionar el botón “Editar”
correspondiente la fila que contiene el jugador que queremos editar.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor11.png) 

Los primeros campos corresponden al puntero del jugador. Esto sólo saldrá si el jugador ya está
grabado previamente en el archivo DBC. Si estamos creando un jugador nuevo estos campos
siempre estarán vacíos. Los punteros se le asignarán al jugador a la hora de guardar el archivo,
teniendo las siguientes opciones:

- Se ha seleccionado un equipo para guardar el archivo DBC: Se utilizarán los punteros
correspondientes para ese equipo (asignados por el editor de forma automática). Por
ejemplo, para el Madrid los punteros son del 151 al 200.
- No se ha seleccionado un equipo para guardar el archivo DBC: Se utilizarán los punteros
desde el 1 al 50.

Del resto de datos sólo serán obligatorios para generar al jugador los marcados en azul oscuro.
El resto de datos los asigna el editor de forma genérica.
Para la generación de las medias, se puede escribir la media total del jugador y el editor se
encargará de generar las medias individuales. Si se deja vacío el campo de media total del
jugador, aunque esté marcad en azul, el editor genera una media aleatoria.

## Abrir Archivo DBC

Desde estas opciones de menú podremos abrir directamente archivos DBC sin pasar por la
pantalla de Generar DBC. Si la carga es correcta se mostrará el equipo en la pantalla de
Generación de DBC para proceder con la edición.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor12.png) 

## Importar información desde la WEB

Al pulsar en el botón “Importar Equipo WEB” del formulario de Generación de DBC se nos
mostrará la siguiente pantalla, desde la cual podremos:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor13.png) 

1: Seleccionar la web desde la que vamos a intentar importar los datos. Actualmente el editor
importa información desde las siguientes webs:

[http://www.footballsquads.com.uk](http://www.footballsquads.com.uk)

[http://www.sofifa.com](http://www.sofifa.com)

[http://www.bdfutbol.com](http://www.bdfutbol.com)

Nota: Sólo desde las 2 últimas se podrán descargar imágenes de jugadores y escudos.

2: Introducir la URL del equipo que queremos actualizar.

3: Seleccionar el nivel de meda que tendrán los jugadores. Para la actualización desde sofifa.com
no se tendrá en cuenta ya que desde esta página podemos importar la media del jugador.

4: Intentar descargar las fotos de los jugadores y escudo del equipo. Los archivos de imagen
descargados se dejarán dentro de la ruta “\Imagenes\Actualizacion \” + nombre largo del
equipo.

Si todo ha ido bien, se mostrarán los resultados en pantalla

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor14.png) 

En el que podremos ver:

1: Datos de la plantilla importada

2: Datos del equipo importado (nombre, nombre largo, entrenador, estadio, capacidad, año de
fundación)

3: Podremos borrar algún jugador de la importación para no incluirlo en la plantilla que llevará
el equipo.

4: Con el botón aceptar traspasamos los datos de esta pantalla a la pantalla de Generación de
DBC para su posterior edición o guardado.

IMPORTANTE: Las fotos quedan almacenadas en el directorio
“\Imagenes\Actualizacion\Nombre_Largo_Equipo\” con el nombre largo de cada jugador. Por
ejemplo, para el Arsenal, desde SOFIFA.COM (https://sofifa.com/team/1/arsenal/)

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor15.png) 

Una vez acabada la importación de datos vemos como se generan las fotos con el nombre largo
de cada jugador. Las imágenes quedarán en este directorio hasta que el usuario lo desee. Pero
al realizar el guardado del archivo DBC el programa busca en este directorio por nombre largo
de jugador y si hay coincidencia genera la foto correspondiente al jugador, es decir la foto
teniendo en cuenta su puntero de guardado.

En este ejemplo, una vez pulsado el botón de aceptar vemos como se ha traspasado la
información a la pantalla de Generación de DBC:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor16.png) 

Una vez presionado el botón de guardar, además de generar el archivo DBC correspondiente se
generan los archivos de foto de jugadores:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor17.png) 

Y lo mismo para el escudo:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor18.png) 

## Edición de competiciones

Podremos editar los equipos presentes en las competiciones de liga correspondientes a los
manager.exe de cada versión soportada por el editor. Además de las competiciones
internacionales. La forma de editar los equipos es directamente sobre los offsets de la posición
hexadecimal en la que están los bytes correspondientes a los equipos, es decir, no se hace una
búsqueda si no que en el editor están definidas las posiciones de los equipos y simplemente se
reemplazan unos equipos con otros. Esto permite abrir cualquier manager.exe editado
previamente por otro usuario.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor19.png) 

Al seleccionar una de las versiones el editor nos pedirá que indiquemos un archivo manager.exe
para leerlo y presentarnos los equipos en pantalla.

Para PC Fútbol 6.0:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor20.png) 

En esta pantalla podremos:

1: Editar los equipos de las divisiones correspondientes a España.

2: Editar las competiciones definidas en el archivo manager.exe (equipos que juegan la
supercopa, la intercontinental, la champions, etc...)

3: Añadir y eliminar equipos de las divisiones. Al pulsar añadir se mostrará un panel para buscar
un equipo.

4: Subir o bajar el orden del equipo dentro de la lista. Esto importa en la versión 6.0 y
extensiones, en las demás da igual ya que el juego ordena los equipos de las divisiones por orden
alfabético ascendiente.

Si presionamos el botón de guardar el archivo con los nuevos cambios estará en la ruta
“\Manager”

Para las competiciones tendremos la siguiente pantalla:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor21.png) 

Pulsando en los botones “...” podremos seleccionar otro equipo.

Lo mismo para el resto de versiones que se pueden seleccionar en el menú. Por ejemplo, para
Argentina:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor22.png) 

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor23.png) 

**IMPORTANTE** : Es necesario que para editar una versión del manager.exe estén cargados los
equipos correspondientes a su archivo de equipos PKF.

## Edición del Calendario

Podremos editar el calendario del juego, esto es, el año de comienzo del juego. Los juegos tienen
fecha de comienzo 1997 o 1998.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor24.png) 

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor25.png) 

Desde esta pantalla podremos:

1: Seleccionar el manager.exe sobre el que se quiere actualizar la fecha. Al seleccionar una
versión el editor abrirá un cuadro de diálogo para que seleccionemos un archivo manager.exe.

2: Aplicar el parche para el efecto 2000

3: En este campo se mostrará la temporada que tiene el manager seleccionado. Esto es por si se
carga un manager que ya esté editado por algún usuario.

4: Selección de la nueva temporada.

Si presionamos el botón de guardar el nuevo archivo manager.exe estará ubicado en la ruta
“\Manager”.

NOTA: El efecto 2000 consiste en que el juego tenía un límite para las edades de los jugadores, de tal forma que si un jugador es nacido en años superiores al 2000 su fecha de nacimiento se determinaba de forma aleatorio sin respetar la fecha que se le asigna al jugador en la edición. Lasignación es totalmente aleatoria, lo cual es un problema para jugadores nacidos más allá del 2000. Para ello hay que sustituir la cadena 6C070000760881FDD0070000 por 01000000760881FDFFFF0000, que es exactamente lo que hace el editor cuando se marca la opción de aplicar el parche para el efecto 2000.

## Selección de Escudos

Para seleccionar el escudo de un equipo y que automáticamente se genere el escudo con el nombre correcto teniendo en cuenta el puntero del equipo se podrá hacer desde 2 lugares:

Desde la pantalla de Generación de archivos DBC

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor26.png) 

Al presionar en el botón “Seleccionar Escudo” se abrirá un cuadro de diálogo para escoger el
archivo de imagen que contiene el escudo. Una vez seleccionado se generará el archivo dentro
de la ruta “\Imagenes\Escudos” con el nombre correcto teniendo en cuenta el puntero del
equipo:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor27.png) 

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor28.png) 

La otra forma es seleccionar el escudo desde la propia pantalla de edición de imágenes

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor29.png) 

Desde este menú se podrán abrir archivos DBC tanto en formato 6.0 como en 5.0. Una vez
cargado el fichero se mostrará la información de la plantilla de jugadores.

De la misma manera que antes, al presionar en “Generar Escudo” se mostrará un cuadro de
diálogo para poder buscar el archivo de imagen que contiene el escudo.

**IMPORTANTE** : Los archivos generados no valen para poner en la carpeta del juego
directamente. Esto es porque no contienen la paleta de colores a 256. Hay que pegarlos sobre
una foto que sí funcione en el juego para que adquiera la paleta correcta. En próximas versiones
del editor intentaré que las imágenes generadas contengan la paleta de colores correcta para
pc fútbol.

## Selección de Fotos de jugadores

Para realizar la selección de fotos de jugadores, y que automáticamente se generen los ficheros
teniendo en cuenta los punteros de los jugadores podremos hacer lo siguiente:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor30.png) 

Desde la pantalla de edición de jugador si presionamos el botón “Seleccionar Foto” se mostrará
un cuadro de diálogo en el que podremos seleccionar la foto del jugador.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor31.png) 

El archivo se guardará en la ruta “\Imagenes\Jugadores” y dentro de este directorio se creará
una carpeta con el nombre del equipo (nombre teniendo en cuenta el puntero del equipo)

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor32.png) 

La otra forma de seleccionar fotos para jugadores es desde el menú de imágenes, cargando un
archivo DBC. Una vez cargado se mostrará la plantilla de jugadores, en la cual podremos
seleccionar una foto para cada jugador. El procedimiento es el mismo, se presiona el botón y se
muestra un cuadro de diálogo en el que se podrá seleccionar una foto. Una vez seleccionada se
guardará en el directorio “\Imagenes\Jugadores”.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor33.png) 

1: Se abrirá un cuadro de diálogo en el que podremos seleccionar una foto para el jugador
correspondiente a la fila pulsada.

2: Pulsando el botón “Generar Foto Estándar” se generará de forma automática una foto
estándar para todos los jugadores de la plantilla. La particularidad de esta foto es que ya tiene
incorporada la paleta de 256 colores de pc fútbol, con lo que basta con copiar los ficheros
generados en el directorio del juego para que las fotos se vean correctamente.

La foto estándar es el archivo “NOFOTO.bmp” que se encuentra en la raíz del programa.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor34.png) 

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor35.png) 

## Actualización masiva desde una web

Uno de los puntos fuertes del editor es poder realizar actualizaciones masivas por lotes de cada
liga de forma individual. Para ello seleccionaremos la opción Actualización del menú:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor36.png) 

Esto nos abrirá la siguiente pantalla en la cual podremos configurar la actualización:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor37.png) 

1: Tendremos que indicar si queremos seleccionar los ficheros para actualizar las ligas o
actualizar directamente las ligas. No podremos actualizar las ligas sin generar antes los ficheros
de actualización. Estos ficheros se generarán dentro de la ruta “\Actualizacion” y se creará un
directorio para cada liga del juego. Dentro de cada directorio correspondiente a cada liga se
creará un fichero que se llamará como el país en concreto y contendrá todos los equipos que
tiene el juego en esa liga.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor38.png) 

Dentro de cada directorio tendremos el archivo que contiene los equipos, por ejemplo para
Bélgica:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor39.png) 

2: Selección de la web desde la cual se va a actualizar de forma masiva.

3: Opciones de actualización

Generar EQ96XXXX.DBC: Si marcamos esta opción el archivo DBC se generará con el nombre
“EQ96” en lugar de “EQ97”.

Usar nombre de equipo para generar el archivo DBC: Si marcamos esta opción se guardará el
archivo usando el nombre real del equipo en lugar de “EQ97XXXX.DBC”

Usar formato 5.0 al guardar el archivo: Si marcamos esta opción se guardará un archivo DBC
respetando el formato de las versiones PCF 5.0.

Intentar descargar las fotos de los jugadores y escudo del equipo. Los archivos de imagen
descargados se dejarán dentro de la ruta “\Imagenes\Actualizacion \” + nombre largo del
equipo. Los archivos de imágenesy escudos con los punteros de jugadores y equipos estarán
en la ruta “\Imagenes\Jugdores” y “\Imagenes\Escudos”.

### Estructura del fichero de liga

Los ficheros generados para realizar la actualización de forma masiva tienen una estructura
que debemos conocer para poder realizar la edición de equipos.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor40.png) 

1: Puntero decimal del equipo. Necesario para generar el archivo DBC de forma automática. No
deberíamos tocar este dato.

2: Nombre del equipo original del juego. Necesario por si se marca la opción de guardar los
ficheros con el nombre del equipo. No deberíamos tocar este dato.

3: Intervalo de medias que queremos que tengan los jugadores. Este dato lo podemos tocar,
tanto la cota inferior como la superior.

4: Puntero desde el que se generarán los jugadores. Necesario para saber desde qué número
asignar punteros y para la generación de fotos (si se ha marcado la opción). No debemos tocar
este dato.

5: Dirección web desde la que se desea actualizar la plantilla.

Podemos editar un archivo entero, para poner las medias y las url de las webs y actualizar esa
liga. Por ejemplo, para Bélgica:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor41.png) 

Adicionalmente tenemos un botón para ver el LOG de errores y avisos.

Si un fichero de una misma liga tiene direcciones web de las 3 webs admitidas por el editor
tendremos que realizar 3 veces el proceso de actualización, seleccionando una web para cada
actualización. El editor comprueba que si has seleccionado footballsquads el link que esté en el
fichero de liga sea de footballsquads.

## Utilidades

Desde este menú podremos realizar las siguientes acciones de forma rápida

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor42.png) 

Abrir las rutas predefinidas para el editor como por ejemplo las rutas de imágenes, generación
de equipos, managers, etc...

Abrir el LOG de la sesión activa del editor.

Vaciar el Log que hay situado en la parte inferior de la pantalla principal del editor.

Vaciar la carpeta de Logs

Lanzar un convertido entre decimal y hexadecimal integrado en el propio editor

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor43.png) 

## Logs

Cada vez que se inicia una sesión del editor se genera un LOG en la carpeta “\Logs”. En este log
se guarda toda interacción del usuario con el editor, además de errores o avisos. Es
especialmente útil cuando se generan equipos desde internet.

En pantalla se muestra un log con mensajes importantes para el usuario. Si hay algún error se
da un mensaje genérico para que se consulte el log para obtener más detalles.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor44.png) 

## Edición hexadecimal de archivos DBC

La explicación será para el formato 6.0 del juego. A continuación, vemos una cadena de un
archivo DBC para un equipo

### Edición de datos del equipo

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor45.png) 

La cadena desglosada con el significado para cada posición de bytes:

- 436F7079726967687420286329313939362044696E616D6963204D756C74696D65646 961 : Separador de Dynamic Multimedia. Es una cadena fija.
- CB0803020000: Cadena constante de comienzo de equipo.
- 0B00 3304000D412C0005130805: Longitud de nombre corto seguido del nombre corto del equipo.
- 1100 32000F150800060E412304130F00038814: Longitud del nombre del estadio seguido del nombre del estadio.
- 16 : Código del país al que pertenece el equipo.
- 1A00 3304000D412C000513080541220D140341050441279B15030E0D: Longitud de nombre largo seguido del nombre largo del equipo.
- E23901: Capacidad del estadio. Para convertirlo a decimal se tienen que dar la vuelta a los bytes, en este ejemplo quedaría 0139E2, lo que pasado a decimal son 80.354.
- 000000000046006900 : Cadena fija con la longitud del terreno de juego.
- 6E07: Año de fundación del club. Para pasarlo a decimal hay que invertir los pares de bytes. En este ejemplo sería 076E, que pasado a decimal es 1902.
- 88E70400: Número de socios del club.
- 0100 4F: Longitud del presidente seguido del nombre del presidente.
- 802500 00 802500 00 : Presupuesto de la base de datos seguido del separador constante “00”, seguido del presupuesto para el juego y seguido por el separador constante “00”. Hay que invertir los 3 pares de bytes para pasarlo a decimal. En este ejemplo sería 002580 lo que equivale a 9600 millones de pesetas. El presupuesto tiene que ir en pesetas.
- 0100 4F: Longitud del patrocinador seguido del nombre del patrocinador.
- 0600 200508050012 : Longitud de la indumentaria seguido del nombre de la indumentaria.
- FFFF: Puntero del equipo filial. Si no hay equipo filial se pone un FFFF.
- FFFF00020005000100050001000A0007000F00010001000000000000000000000000000000000B020202020 302010101010101010101010101020101010101010103030404040301010101010000000000000000000000000000000000000201000000000000000000000000000000000000000000000000000000000000 : Cadena con los datos del equipo en lo respectivo a comentarios y competiciones. En el editor esta cadena siempre será fija.
- 000042002A004200000058000000580000008400B00042002E009E008000A70000000000D40058002D0012007E00070000002E0087006A002A006E0066006F0000002B0085006D002A00420062003F002700250095007A00410056008E006900600036009B00600076005A00D6005B0060006100920063006A008400D1007E007A002C00C4006E00910049000A0161004B00140098004F0061002A00BC002A0090000000AD006E0093002A000B013D00: Táctica definida para el equipo.
- 4F1E0201000101: Táctica de equipo
- 02 : Comienzo de la cadena de entrenador. Es una cadena fija.
- 0400 : Puntero del entrenador.
- 0600 3B0805000F04: Longitud del nombre corto del entrenador seguido del nombre corto del entrenador.
- 1500 3B080F0405080F044138001B0805413B2825202F24: Longitud del nombre largo seguido del nombre largo del entrenador.
- 01001901001901001901001901001910002F254D2F254D2F254D2F254D2F256C6B031 0002F254D2F254D2F254D2F254D2F256C6B010019: Cadena fija después del nombre largo del entrenador.

Después de este dato vendrían los datos de los jugadores.

### Edición de datos de jugadores

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor46.png) 

- 01 : Cadena fija que marca el comienzo de la cadena de jugador. Es la misma para todo jugador.
- 5B00: Puntero del jugador. No puede repetirse dentro de un mismo equipo.
- 01 : Dorsal del jugador.
- 0800 220E1413150E0812: Longitud del nombre corto seguido del nombre corto del jugador.
- 1D00 35090803001415412F08020E0D0012412C00130241222E3433352E2832: Longitud de nombre largo seguido del nombre largo del jugador.
- 01 : Slot que ocupa en el equipo.
- 00 : Procedencia del jugador. 00 Indica que continua. El editor siempre pondrá un 00 por defecto.
- 010000000000 : Cadena de roles del jugador. Los posibles valores son 00 Vacío, 01 Portero, 02 Lateral derecho, 03 Lateral izquierdo, 04 Libre, 05 Central izquierdo, 06 Central derecho, 07 Centrocampista derecha, 08 Interior derecho, 09 Delantero centro, 0A Medio centro organizador, 0B Centrocampista izquierda, 0C Extremo derecho, 0D Media punta por el centro, 0E Extremo izquierdo, 0F Medio centro defensivo, 10 Media punta derecha, 11 Media punta izquierda y 12 Interior izquierdo. 
- 0C: Nacionalidad del jugador. Consultar la lista de códigos de países para conocer la correspondencia entre códigos y países.
- 01 : Color de piel del jugador. Los posibles valores son 01 blanco, 02 negro o 03 mulato.
- 06 : Color de pelo del jugador. Los posibles valores son 01 rubio, 02 sin pelo, 03 moreno, 04 blanco o canoso, 05 pelirrojo y 06 castaño.
- 00 : Demarcación correspondiente al jugador. Los posibles valores son 00 Portero, 01 Defensa, 02 Medio o 03 Delantero.
- 0B05C807: Fecha de nacimiento del jugador. Compuesta por Día, Mes y año respectivamente.
- C7: Altura correspondiente al jugador.
- 60 : Peso correspondiente al jugador.
- 0C: País de nacimiento del jugador.
- 0E00 23130404414923880D0608020048: Longitud del lugar de nacimiento seguido del lugar de nacimiento.
- 01004F01004F01001901001901001901001901001901001910002F254D2F254D2F254D2F254D2F256C6B: Cadena fija.
- 5654525C0D0E15191256: Medias del jugador, por este orden VE velocidad, RE resistencia, AG agresividad, CA calidad, RM remate, RG regate, PA pase, TI tiro, EN
entradas y PO portero.

### Diferencia entre archivos con formato 5.0 y formato 6.0

El editor permite generar archivos con formato para versiones 5.0 o para versiones 6.0. Las diferencias entre ambos formatos son:

- La cadena de comienzo de equipo es diferente:

Para el 5.0: FB079F010000
Para el 6.0: CB0803020000

- La cadena de las dimensiones del campo es diferente:

Para el 5.0: 0000000046006900
Para el 6.0: 000000000000000046006900

- El orden de las medias es diferente:

Para el 5.0: VE, RE, AG, CA, RG, RM, PA, TI, EN, PO
Para el 6.0: VE, RE, AG, CA, RM, RG, PA, TI, EN, PO

Nota: Además de esto cambia alguna cadena que expongo como fija, como por ejemplo la cadena de comentarios del jugador. Lo mejor es generar un mismo equipo con el editor tanto en formato 5 como en 6 y ver las diferencias entre los archivos.



