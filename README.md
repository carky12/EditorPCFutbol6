# EDITOR PC FÚTBOL 6.0

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/Fondo.bmp) 

#### Creado por carky12

## Breve Descripción

En este documento se exponen las explicaciones necesarias para poder utilizar el editor de pc fútbol 6.0. 

El editor es válido para versiones 
- PC FÚTBOL 5.0
- PC FÚTBOL 5.0 EXTENSION 1
- PC FÚTBOL 5.0 EXTENSION 2
- PC FÚTBOL 5.0 EDICIÓN ORO
- PC FÚTBOL 6.0
- PC FÚTBOL 6.0 EXTENSION 1
- PC FÚTBOL 6.0 EXTENSION 2
- PC FÚTBOL 6.0 PLUS
- PC FÚTBOL 6.0 EDICIÓN ORO
- PC FRANCE 5.0
- PC PREMIER 6.0
- PC CALCIO 5.0
- PC CALCIO 6.0
- PC APERTURA 5.0 (97)
- PC APERTURA 5.0 (98)

El manual completo (con capturas y en PDF) está en este enlace: [Manual Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Manuales/Manual%20Editor%20PCF%C3%BAtbol%206.pdf)

Podéis ver los videos del Editor funcionando en los siguientes enlaces de YouTube:

[Edición de competiciones](https://www.youtube.com/watch?v=SMxl0EtCkTs&feature=youtu.be&ab_channel=CarlosGonz%C3%A1lez)

[Generación de archivos DBC](https://www.youtube.com/watch?v=ChxB0d5TN6Y&feature=youtu.be&ab_channel=CarlosGonz%C3%A1lez)

[Actualzación masiva desde una web](https://www.youtube.com/watch?v=IAcNQdtkJOE&feature=youtu.be&ab_channel=CarlosGonz%C3%A1lez)

<!--
## Dedicatoria

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/dedicatoria1.png) 
![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/dedicatoria4.png) 

Quisiera dedicar este proyecto a todo el mundo que durante este año ha perdido a alguien. Ha sido un año muy duro para todos, en el que hemos perdido, y no solo hemos perdido cercanos, hemos perdido leyendas, que de una manera u otra han marcado a una generación entera (mi generación).

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/dedicatoria6.png) 
![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/dedicatoria5.png) 
![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/dedicatoria7.jpg) 

No voy a nombrar a ninguno de los grandes que se han ido en este 2020, por que sería injusto con respecto a los que se han ido y no son nombrados. Sin más mucha fuerza todos y ánimo para este 2021!
-->
## Índice

- [Introducción](#introducción).
- [Versiones del juego aceptadas por el editor](#versiones-del-juego-aceptadas-por-el-editor)
- [Rutas que utiliza el editor](#rutas-que-utiliza-el-editor)
- [Cargar archivo de equipos](#cargar-archivo-de-equipos)
- [Generar DBC Originales](#generar-dbc-originales)
- [Edición de Equipos](#edición-de-equipos)
- [Edición de Jugadores](#edición-de-jugadores)
- [Importar información desde la WEB](#importar-información-desde-la-web)
- [Edición de competiciones](#edición-de-competiciones)
- [Edición del Calendario](#edición-del-calendario)
- [Selección de Escudos](#selección-de-escudos)
- [Selección de Fotos de jugadores](#selección-de-fotos-de-jugadores)
- [Actualización masiva desde una web](#actualización-masiva-desde-una-web)
- [Intercambio de jugadores](#intercambio-de-jugadores)
- [Juveniles](#juveniles)
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

Para poder usar el editor tenéis que tener instalado una versión reciente del .NET Framework de Microsoft.

## Versiones del juego aceptadas por el editor

El editor funciona para las siguientes versiones del juego:

- PC Fútbol 6.0: Archivo de equipos EQ022022.PKF. Tamaño del manager 2556 KB.
- PC Fútbol 6.0 Extensión 1: Archivo de equipos EQ022022.PKF. Tamaño del manager 2569 KB.
- PC Fútbol 6.0 Extensión 2: Archivo de equipos EQPCPLUS.PKF. Tamaño del manager 2486 KB.
- PC Premier 6.0: Archivo de equipos EQ030022.PKF. Tamaño del manager 2771 KB.
- PC Calcio 6.0: Archivo de equipos EQ036022.PKF. Tamaño del manager 2513 KB.
- PC Apertura 6.0: Archivo de equipos EQ003003.PKF. Tamaño del manager 2397 KB.
- Cualquier versión de PC Fútbol 5.0 (original, extensiones y edición oro).
- Además, funciona con versiones raras basadas en PC Fútbol 5 y 6 como por ejemplo PC River o PC Real Madrid.

En estas versiones se pueden editar lo siguiente:

Generación de equipos
Generación de equipos.
- Edición de equipos a partir de un archivo DBC.
- Edición de jugadores contenidos en un archivo DBC.
- Edición de los archivos originales del juego.
- Generación de equipos de juveniles.
- Intercambio de jugadores entre dos archivos DBC.
- Edición de las competiciones del archivo manager.exe.
- Edición del año de comienzo del juego.
- Seleccionar fotos para jugadores.
- Seleccionar escudos para equipos.
- Actualización automática de equipos desde una página de internet.

El editor permite guardar archivos DBC válidos para cualquier versión 5.0 y 6.0 del juego.

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

## Generar DBC Originales

Con esta opción podremos generar todos los archivos DBC correspondientes a los equipos originales del juego. Estos archivos contendrán los datos (jugadores, entrenadores y datos de la base de datos) originales del juego.

Al realizar la carga se nos pedirá que seleccionemos un archivo PKF original para comenzar la generación.

Esta opción permite con la edición posterior del archivo DBC correspondiente editar la información contenida en los equipos originales del juego.

Los ficheros DBC se generarán dentro de la ruta de “EquiposDBC” del editor, y dentro de esta en una carpeta llamada con el archivo PKF que se seleccionó para la carga.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor1-1.png) 

Con esta opción se generan los archivos DBC para todos los equipos contenidos en el archivo PKF. Posteriormente veremos un método para generar solo un fichero DBC para un equipo concreto.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor1-2.png) 

## Edición de Equipos

Se podrá consultar los equipos originales del archivo PKF, editar un equipo desde un fichero DBC,
o generar un fichero DBC nuevo.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor2.png) 

### Consulta de equipos

Desde esta pantalla podremos consultar los equipos contenidos en el archivo PKF cargado al
inicio. Esto nos puede ser útil para conocer su puntero (tanto en formato decimal como en
formato hexadecimal).

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor3.png) 

Desde esta pantalla podremos realizar la búsqueda de equipos por nombre, puntero (si es que conocemos su puntero) o por país.

Además, podremos generar un archivo DBC correspondiente al equipo seleccionado en la lista, con el objetivo de su posterior edición. Este archivo DBC contendrá toda la información del equipo seleccionado, es decir, los datos del equipo, los datos de sus jugadores y además toda la información contenida en la base de datos para del juego de su entrenador y jugadores.

Podremos guardar el fichero DBC utilizando el nombre del equipo marcando la opción correspondiente.

En la lista de equipos se informa de si el equipo corresponde a una liga extranjera o es de tipo nacional. Esto influye en el nivel de información que llevará el fichero. Un fichero de liga nacional podrá contener información que se muestra en la base de datos del juego, como el perfil del entrenador, anécdotas, declaraciones, etc…

Dependiendo de la versión un equipo puede ser de liga nacional o de liga extranjera, por ejemplo, para la versión argentina los equipos nacionales (los que contienen información de base de datos) son los que tienen el país Argentina. Estos mismos equipos en la versión Premier por ejemplo están considerados como de liga extranjera, no guardando por tanto ninguna información de base de datos. A la hora de guardar un archivo DBC el editor nos permite generar el archivo como si fuese para liga extrajera o para liga nacional, o ambos ficheros a la vez.

### Abrir archivo DBC

Con esta opción podremos cargar un archivo DBC para su posterior edición. El editor será capaz de identificar si se trata de un DBC de PCF 5.x o PCF 6.x y cargará todos los datos del equipo para su edición.

#### Error valor de letra no conocido

A la hora de abrir un archivo DBC nos puede dar un error de “Valor de letra no conocido”. Esto es debido a que hay algún par de bytes del archivo DBC que no se reconocen para traducirlos a lenguaje decimal. Esto es debido a que en la información original del juego se cometió algún error y el carácter utilizado no es el correcto.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/error_valor_desconocido.png) 

Para solucionar este tipo de errores tendremos que hacer lo siguiente:
- Abrir el archivo DBC con un editor hexadecimal. Aconsejable HexWorkshop.
- Utilizar el archivo de mapa correspondiente al PC Fútbol (es un mapa de PC Fútbol Site).
- Buscar dentro del archivo los pares de bytes desconocidos (en el caso del ejemplo sería “3F”).

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/error_valor_desconocido_2.png) 

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/error_valor_desconocido_1.png) 

- Una vez encontrado nos quedaremos con el valor en decimal, que sale en la parte derecha del editor hexadecimal. En el caso del ejemplo el símbolo será un “^”.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/error_valor_desconocido_3.png) 

- Abriremos el archivo map.txt, situado en la raíz de la carpeta del editor y añadiremos el valor encontrado. En este caso hay que añadir “3F : ^”.
- Una vez hecho esto repetiremos la carga del archivo DBC, y ya no debería dar el error.

### Nuevo archivo DBC

Desde esta pantalla podremos generar un archivo DBC de múltiples formas. Podremos cargar
un archivo DBC existente y cambiar lo que necesitemos, podremos generar un archivo DBC
totalmente desde cero y también podremos importar datos desde una web.

#### Pestaña de Equipo

Desde aquí podremos definir todos los datos generales de un equipo. Los campos marcados en
azul oscuro son obligatorios, los demás los guarda el propio editor de forma predeterminada.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor4.png) 

Para guardar el fichero tendremos las siguientes opciones.

1: Generar EQ96XXXX.DBC: Si marcamos esta opción el archivo se generará con el nombre “EQ96” en lugar de “EQ97”.

2: Usar nombre de equipo para generar el archivo DBC: Si marcamos esta opción se guardará el archivo usando el nombre real del equipo en lugar de “EQ97XXXX.DBC”

3: No guardar información de base de datos del juego: Si marcamos esta opción se guardará el equipo sin tener en cuenta la información de base de datos, esta opción sólo es útil para equipos de Liga Nacional (que tengan el campo Liga Extranjera NO) ya que es para los únicos para los que se puede grabar información de base de datos. Si marcamos esta opción por tanto no se guardará la información de base de datos relativa a información de jugadores, entrenadores y datos de competiciones, y en su lugar se guardará una cadena genérica con una “x”.

4: Generar versiones nacional y extranjera: Esta opción nos permitirá guardar 2 archivos DBC, uno con el formato de equipo de liga nacional y otro con formato de liga extranjera. Esto puede ser útil cuando estamos editando varias versiones del juego. Por ejemplo, para la versión española el Sevilla debería tener el campo Liga Extranjera NO, pero para la versión argentina debería tener Liga Extranjera SI. Dependiendo de si es un equipo de Liga Extranjera o no se guardará más o menos información en el fichero DBC. Por tanto, con esta opción podemos generar los dos ficheros con de una sola tacada. Los ficheros generados tendrán el nombre que hayamos elegido (nombre del equipo o nombre con formato PCF, es decir EQXXXXXX.DBC) seguido de de los literales “_BBDD.DBC” para los equipos creados de liga nacional, y “_NO_BBDD.DBC” para los equipos creados de liga extranjera.

5: Utilizar punteros propios del DBC para los jugadores: Esta opción sólo estará disponible si cargamos un fichero DBC. Si marcamos esta opción no se utilizarán los punteros para los jugadores sugeridos por el editor, sino que se respetarán los punteros de jugadores que ya tuviese el fichero DBC.

En la parte superior podemos ver los campos de los punteros. Estos campos no son editables. Si están vacíos se guardará el fichero DBC con el nombre EQ970000.DBC, y los para los punteros de los jugadores se utilizarán de forma consecutiva desde el número 1.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor5.png) 

Si pulsamos en el botón con los “...” se mostrará una ventana en la que podremos seleccionar un equipo. En esta ventana se muestran los equipos originales del archivo PKF cargado al inicio.
En dicha ventana podremos buscar un equipo por nombre.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor6.png) 

Al seleccionar un equipo se mostrará:

1: el puntero decimal

2: el puntero hexadecimal

3: el nombre del equipo y el nombre del fichero DBC que resultará al guardar

4: los punteros de jugadores que se utilizarán. Se reservan 49 punteros para cada equipo, empezando en el primer equipo (Barcelona) que se reservan los punteros del 1 al 50, para el segundo equipo (Deportivo) del 51 al 100, y así hasta el último equipo. Si se marca la opción de “Utilizar punteros propios del archivo DBC para jugadores” no se generarán los punteros sugeridos por el editor si no que se respetarán los que tenga el fichero cargado.

**IMPORTANTE** : Al cargar un fichero, se intenta buscar el puntero entre la lista de equipos originales cargados (archivo PKF). Si por lo que fuese no se encuentra el puntero y se guarda de nuevo el fichero DBC se sobrescribirán los punteros de jugadores. Ejemplo: Si tienes un fichero EQ970004.DBC al cargarlo se realizará la búsqueda de cuál es el equipo que tiene e puntero “0004” decimal. Resultará el Real Madrid, con lo que se rellenarán los campos correspondientes y los punteros de jugadores serán los mismos, es decir, del 151 al 200. Si el archivo que cargamos se llama EQ979999.DBC, no se encontrará ningún equipo con puntero decimal “9999” por lo que los punteros de jugadores que se utilizarán al guardar este fichero serán del 1 al 50.

#### Pestaña de Tácticas

Desde aquí podremos editar la táctica que utilizará el equipo. Por defecto, si no seleccionamos
nada se guarda lo que se muestra en la captura.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor7.png) 

Desde aquí podremos editar la táctica que utilizará el equipo. Por defecto, si no seleccionamos nada se guarda el sistema 442 y los valores por defecto para las tácticas de equipo.

Además de las tácticas predefinidas podremos cargar una táctica personalizada para el equipo, seleccionando un fichero que contenga una táctica válida.

Cuando se carga un fichero DBC se identifica la táctica que tiene, y si no coincide con ninguna de las tácticas predefinidas se marcará la opción “El equipo tiene una Táctica Personalizada”.

#### Pestaña Plantilla

Desde esta pestaña podremos consultar la plantilla de jugadores que hay en el archivo DBC
además de crear un jugador nuevo.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor8.png) 

La lista de jugadores se ordenará por demarcación, siguiendo este orden: primero los porteros, después los defensas, los medios y por último los delanteros. Pulsando el botón “Nuevo” accederemos a la pantalla de creación de jugadores.

En la lista podremos consultar el nombre corto del jugador, el nombre largo del jugador, la media global, la demarcación, podremos acceder a la edición de sus datos y borrarlo de la plantilla.

**IMPORTANTE**: Debido a la ordenación de los jugadores en la lista si tenemos un equipo con 25 jugadores con sus respectivos punteros, y añadimos un portero, se recalcularán los punteros de los 26 jugadores (ya que se ha incrustado un jugador en medio de otros ya existentes). Hay que tener esto en cuenta por si tenemos fotos de jugadores asociados a punteros de equipos ya guardados. Por eso lo mejor es dejar la edición de las fotos para cuando se tengan todos los equipos perfectamente actualizados.

Desde esta pestaña estará disponible un menú contextual para facilitar la edición. Sobre un jugador que esté seleccionado en la grid de jugadores al pulsar con el botón derecho del ratón nos saldrá un menú en el que podremos realizar las siguientes acciones:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor8-1.png) 

Nuevo jugador: Nos llevará a la pantalla para crear un nuevo jugador.

Editar jugador: Nos llevará a la pantalla de edición de jugadores con los datos del jugador seleccionado cargados para poder editarlos.

Borrar jugador: borrará el jugador de la plantilla del equipo.

Copiar jugador: Creará una copia exacta del jugador seleccionado. El puntero del nuevo jugador se copiará vacío, para que al guardar el equipo se le asigne uno.

El límite de jugadores por equipo es de 35, salvo para los equipos de juveniles que el límite será de 98.

#### Pestaña de Datos de Competiciones

Desde esta pestaña podremos consultar y editar los datos de competiciones del equipo. Esta pestaña sólo estará visible si el equipo tiene el campo Liga Extranjera a NO. Esta información se podrá visualizar en la base de datos del juego. Si no se cubre nada el editor genera unos datos por defecto.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor8-2.png) 

La cadena de Palmarés no se ha desarrollado de forma visual ya que es totalmente dependiente de la versión del juego para el que se cree el archivo DBC. Por tanto, hay que conocer la estructura de la cadena para saber qué información poner. Por ejemplo, para la versión española los cuatro primeros bytes corresponden a la copa del rey. Lo único a tener en cuenta es que la cadena de palmarés, para los archivos DBC que genera el editor, tiene que medir 68 caracteres.

#### Pestaña de Datos de Entrenador

Desde esta pestaña podremos consultar y editar los datos del entrenador del equipo. Esta pestaña sólo estará visible si el equipo tiene el campo Liga Extranjera a NO. Esta información se podrá visualizar en la base de datos del juego. Si no se cubre nada el editor genera unos datos por defecto.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor8-3.png) 

### Acciones que se pueden realizar

Desde la pantalla de edición de equipos se pueden realizar las siguientes acciones

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor9.png) 

1: Añadir un nuevo jugador a la plantilla. Al pulsar este botón se accede a la pantalla de edición de jugador.

2: Editar las características de un jugador de la plantilla. Al pulsar este botón se accede a la pantalla de edición de jugador.

3: Borrar un jugador de la plantilla.

4: Guardar un archivo DBC: Guarda la información del equipo en un fichero DBC.

5: Cargar un archivo DBC. Se muestra un cuadro de diálogo en el que se podrá seleccionar un fichero DBC.

Ejemplo: Al cargar el fichero “EQ970004.DBC” se busca en los equipos originales y se encuentra al Real Madrid:

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor10.png) 

De esta forma nos desentendemos de la gestión de los punteros, simplemente hay que ser un poco organizados con la edición y el editor se encarga del resto.

6: Importar información desde la web. Al pulsar este botón se accede a la pantalla de importar información.

7: Seleccionar una imagen de escudo para el equipo. Se muestra un cuadro de diálogo en el que se podrá seleccionar un fichero DBC.

## Edición de Jugadores

Podremos editar cualquier jugador contenido en un fichero DBC. Para editar a un jugador hay que cargar primero el archivo DBC y desde la pestaña plantilla presionar el botón “Editar” correspondiente la fila que contiene el jugador que queremos editar.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor11.png) 

Los primeros campos corresponden al puntero del jugador. Esto sólo saldrá si el jugador ya está grabado previamente en el archivo DBC. Si estamos creando un jugador nuevo estos campos siempre estarán vacíos. Los punteros se le asignarán al jugador a la hora de guardar el archivo, teniendo las siguientes opciones:
- Se ha seleccionado un equipo para guardar el archivo DBC: Se utilizarán los punteros correspondientes para ese equipo (asignados por el editor de forma automática). Por ejemplo, para el Madrid los punteros son del 151 al 200.

- No se ha seleccionado un equipo para guardar el archivo DBC: Se utilizarán los punteros desde el 1 al 50.

- Utilizar los punteros de los jugadores ya grabados en el archivo DBC. Se respetarán los punteros de los jugadores del archivo cargado.

Del resto de datos sólo serán obligatorios para generar al jugador los marcados en azul oscuro. El resto de datos los asigna el editor de forma genérica.
Para la generación de las medias, se puede escribir la media total del jugador y el editor se encargará de generar las medias individuales. Si se deja vacío el campo de media total del jugador, aunque esté marcad en azul, el editor genera una media aleatoria.

Si el jugador pertenece a un equipo de una Liga Nacional (campo Liga Extranjera NO) tendremos disponible una pestaña con Datos del Jugador. En esta pestaña podremos editar la información que se guarda del jugador y es mostrada en la base de datos del juego.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor11-1.png) 

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

[http://www.bdfa.com](http://www.bdfa.com)

Nota: Sólo desde las webs de bdfutbol y sofifa se podrán descargar imágenes de jugadores y escudos.

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

Si queremos editar el calendario de una versión diferente a las mostradas en las opciones (por ejemplo, los manager de las versiones ORO) siempre tendremos que seleccionar la opción “OTROS”. Esto nos obliga a tener que cambiar siempre desde el archivo manager original, debido a que el editor no sabe los offsets que hay que tocar para otros archivos a los expuestos en las opciones de pantalla.

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

Las fotos seleccionadas se transformarán a 32x32 pixeles.

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

## Intercambio de jugadores

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor41-1.png) 

Seleccionando esta opción accederemos a la pantalla que nos permitirá intercambiar jugadores entre dos archivos DBC.

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor41-2.png) 

1 y 2: Presionando este botón cargaremos la plantilla del equipo correspondiente al archivo DBC seleccionado.

3: Se pasará el jugador seleccionado del equipo de la izquierda al de la derecha.

4: Se pasará el jugador seleccionado del equipo de la derecha al de la izquierda.

5: Se intercambiarán los jugadores seleccionados.

6 y 8: Se guardará la información de cada equipo en su correspondiente fichero DBC.

7 y 9: Se muestra la información correspondiente a los punteros que asigna el editor a dicho equipo.

**Importante**: Cuando se intercambia un jugador entre equipos se respeta el puntero que tiene el jugador, es decir no se genera un puntero nuevo, se guarda la información del jugador en el nuevo equipo respetando el puntero que el jugador ya traía del otro equipo.

## Juveniles

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor41-3.png) 

Desde estas opciones de menú accederemos a la edición de equipos. La pantalla es la misma a la que accedemos desde la opción equipos del menú. Con la diferencia de que lo que se creará es un DBC de juveniles. Un archivo DBC de juveniles carece de la información de base de datos, además de que el límite de jugadores es de 150.

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

- 436F7079726967687420286329313939362044696E616D6963204D756C74696D65646961: Separador de Dynamic Multimedia. Es una cadena fija.
- FE06: Primeros bytes del archivo. Se tomarán como cadena fija.
- FE01: Cadena que indica la versión del fichero generado. La versión del fichero influye en la cantidad de información que contiene.
- 00: Idioma del fichero (español, inglés, etc…). El editor siempre guardará 00 correspondiente al idioma español.
- 00: Indica si el equipo es un equipo de liga nacional (jugable) o pertenece a una liga extranjera. Si pertenece a una liga extranjera toda la información de base de datos relativa a entrenador y jugadores no se guardará. En este caso es un fichero de liga nacional (00. Liga extranjera sería 01).
- 1000 3304000D412C000513080541224F274F: Longitud de nombre corto seguido del nombre corto del equipo. En este caso “Real Madrid C.F.” que ocupa 16 caracteres es decir 0010 en hexadecimal.
- 1100 32000F150800060E412304130F00038814: Longitud del nombre del estadio seguido del nombre del estadio. En este caso “Santiago Bernabéu”.
- 16: Código del país al que pertenece el equipo. Consultar la lista de códigos de equipo.
- 1A00 3304000D412C000513080541220D140341050441279B15030E0D: Longitud de nombre largo seguido del nombre largo del equipo.
- D85301: Capacidad del estadio. Para convertirlo a decimal se tienen que dar la vuelta a los bytes, en este ejemplo quedaría 0153D8, lo que pasado a decimal son 87.000.
- 00: Separador de cadena fijo.
- 000000: Capacidad del estadio para aforo de pie. Para convertirlo a decimal se tienen que dar la vuelta a los bytes.
- 00: Separador de cadena fijo.
- 46006A00: Cadena fija con la longitud del terreno de juego. En este caso 70 x 106.
- 6E07: Año de fundación del club. Para pasarlo a decimal hay que invertir los pares de bytes. En este ejemplo sería 076E, que pasado a decimal es 1902.
- 701101: Número de socios del club. Para pasarlo a decimal hay que invertir los bytes, quedando 011170 lo que en decimal corresponde a 70.000.
- 00: Separador de cadena fijo.
- 1400 2D0E13040F1B0E4132000F1B412C000F0204030E: Longitud del presidente seguido del nombre del presidente. En este caso “Lorenzo Sanz Mancebo”.
- 504600: Presupuesto para el juego del equipo. En este caso, invirtiendo los bytes queda 004650, que corresponde a 18.000 millones. El presupuesto va en pesetas.
- 00: Separador de cadena fijo.
- 504600: Presupuesto real del equipo. El editor guardará el mismo valor que el del presupuesto del juego.
- 0400 35242A20: Longitud del patrocinador seguido del nombre del patrocinador. En este caso “TEKA”.
- 0600 202528252032: Longitud de la indumentaria seguido del nombre de la indumentaria. En este caso “ADIDAS”.
- FFFF: Puntero del equipo filial. Si no hay equipo filial se pone un FFFF.
- FFFF: Puntero del equipo filial 2. Si no hay equipo filial se pone un FFFF.
- 01: Grupo de 2ºB al que pertenecería en caso de descenso. Para equipos que no sean de España se guarda un 00 (o se puede guardar cualquier valor, el juego no lo leerá).
- 0100010001000100010001000100010001000100: Puesto de las últimas 10 ligas. Los bytes se separan en parejas PUESTO-LIGA, siendo los 2 primeros el puesto y los dos siguientes la liga jugada (00 es primera división, 01 es segunda división, 02 es segunda división b y 03 es tercera división). Por ejemplo, la pareja 0501 indica que el equipo quedó quinto en segunda división. La cadena ocupa 40 caracteres.
- 00: Cadena que indica el número de temporadas en primera división.
- 0000: Indica el número de partidos jugados. Hay que darles la vuelta a los bytes para convertirlo a decimal.
- 0000: Indica el número de partidos ganados. Hay que darles la vuelta a los bytes para convertirlo a decimal.
- 0000: Indica el número de partidos empatados. Hay que darles la vuelta a los bytes para convertirlo a decimal.
- 0000: Indica el número de goles a favor. Hay que darles la vuelta a los bytes para convertirlo a decimal.
- 0000: Indica el número de goles en contra. Hay que darles la vuelta a los bytes para convertirlo a decimal.
- 0000: Indica el número de puntos conseguidos. Hay que darles la vuelta a los bytes para convertirlo a decimal.
- 00: Indica el número de veces que el equipo fue campeón.
- 00: Indica el número de veces que el equipo fue subcampeón.
- 00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000: Cadena que indica las posiciones del equipo en las jornadas de la base de datos. Cadena que ocupa 92 caracteres. El editor siempre guarda esta cadena a ceros.
- 00000000000000000000000000000000000000000000000000000000000000000000: Indica la cadena del palmarés del equipo en todas las competiciones. La cadena ocupa 34 caracteres.
- 000042002A004200000058000000580000007E00F80045003B00A200BF00A000000000003E0142003B000B00B300170000004A00B000640021006F0073007B0000000000B100650022003C007000380022002D00FF006C0051004100C0004A006D005400D00071006D009A000201A70053003600EA005D0086003F0006013C006C003000D10075008A006A0016015A0043004900FA004A0052006000DB006D002E000000E000640070001900F5000600: Táctica definida para el equipo.
- 46390001000001: Táctica de equipo. Se divide en:
- - 46: Porcentaje de toque. En este aso 70%.
- - 39: Porcentaje de contragolpe. En este caso 57%.
- - 00: Tipo de ataque. (00 ofensivo, 01 especulativo y 02 mixto)
- - 01: Tipo de entradas. (00 suave, 01 media y 02 agresiva)
- - 00: Marcaje. (00 zona y 01 hombre)
- - 00: Despejes. (00 jugado y 01 largo)
- - 01: Tipo de presión. (00 propio, 01 medio y 02 rival
- 02: Comienzo de la cadena de entrenador. Es una cadena fija.
- 6906: Puntero del entrenador.
- 0700 29080505080F0A: Longitud del nombre corto del entrenador seguido del nombre corto del entrenador. En este caso “Hiddink”.
- 0C00 261414124129080505080F0A: Longitud del nombre largo seguido del nombre largo del entrenador. En este caso “Guus Hiddink”.
- 0100 19: Longitud de perfil de entrenador seguido del perfil de entrenador. En este caso es “x” que es el valor por defecto que grabará el editor.
- 0100 19: Longitud de los sistemas habituales del entrenador seguido de los sistemas habituales del entrenador. En este caso es “x” que es el valor por defecto que grabará el editor.
- 0100 19: Longitud del palmarés de entrenador seguido del palmarés de entrenador. En este caso es “x” que es el valor por defecto que grabará el editor.
- 0100 19: Longitud de las anécdotas del entrenador seguido de las anécdotas del entrenador. En este caso es “x” que es el valor por defecto que grabará el editor.
- 0100 19: Longitud de la información de la última temporada del entrenador seguido de la información relativa a la última temporada del entrenador. En este caso es “x” que es el valor por defecto que grabará el editor.
- 1000 2F254D2F254D2F254D2F254D2F256C6C: Longitud de la trayectoria del entrenador seguido de la trayectoria del entrenador. Esta es la cadena por defecto que grabará el editor y corresponde a los valores en decimal “ND,ND,ND,ND,ND==”.
- 03: Separador que indica que el entrenador tiene trayectoria como jugador. Si esta pareja de bytes no es 03 se saltaría a las declaraciones del entrenador.
- 1000 2F254D2F254D2F254D2F254D2F256C6C: Longitud de la trayectoria del entrenador como jugador seguido de la trayectoria del entrenador como jugador. Esta es la cadena por defecto que grabará el editor y corresponde a los valores en decimal “ND,ND,ND,ND,ND==”.
- 0100 19: Longitud de las declaraciones del entrenador seguido de las declaraciones del entrenador.

Notas sobre las versiones de archivos DBC: Pueden darse las siguientes excepciones:
- Latitud del estadio: Par de bytes que van después del país del equipo que indican la latitud en la que se encuentra el estadio. El editor está preparado para leer estos bytes, aunque la versión que genera de los DBC nunca grabará dichos bytes.
- Capacidad del estadio de pie: Dependiendo de la versión del archivo DBC la capacidad del estadio de pie puede aparecer o no. El editor está preparado para leer estos ficheros, y la versión de archivos DBC que genera contiene los bytes correspondientes a la capacidad del estadio de pie.

Después de este dato vendrían los datos de los jugadores.

### Edición de datos de jugadores

![Editor PCF 6.0](https://github.com/carky12/EditorPCFutbol6/blob/master/Imagenes/editor46.png) 

01: Cadena fija que marca el comienzo de la cadena de jugador. Es la misma para todo jugador.
- 5B00: Puntero del jugador. No puede repetirse dentro de un mismo equipo.
- 01: Dorsal del jugador.
- 0800 220E1413150E0812: Longitud del nombre corto seguido del nombre corto del jugador.
- 1D00 35090803001415412F08020E0D0012412C00130241222E3433352E2832: Longitud de nombre largo seguido del nombre largo del jugador.
- 01: Slot que ocupa en el equipo.
- 00: Procedencia del jugador. 00 Indica que continua. El editor siempre pondrá un 00 por defecto.
- 010000000000: Cadena de roles del jugador. Los posibles valores son 00 Vacío, 01 Portero, 02 Lateral derecho, 03 Lateral izquierdo, 04 Libre, 05 Central izquierdo, 06 Central derecho, 07 Centrocampista derecha, 08 Interior derecho, 09 Delantero centro, 0A Medio centro organizador, 0B Centrocampista izquierda, 0C Extremo derecho, 0D Media punta por el centro, 0E Extremo izquierdo, 0F Medio centro defensivo, 10 Media punta derecha, 11 Media punta izquierda y 12 Interior izquierdo.
- 0C: Nacionalidad del jugador. Consultar la lista de códigos de países para conocer la correspondencia entre códigos y países.
- 01: Color de piel del jugador. Los posibles valores son 01 blanco, 02 negro o 03 mulato.
- 06: Color de pelo del jugador. Los posibles valores son 01 rubio, 02 sin pelo, 03 moreno, 04 blanco o canoso, 05 pelirrojo y 06 castaño.
- 00: Demarcación correspondiente al jugador. Los posibles valores son 00 Portero, 01 Defensa, 02 Medio o 03 Delantero.
- 0B05C807: Fecha de nacimiento del jugador. Compuesta por Día, Mes y año respectivamente.
- C7: Altura correspondiente al jugador.
- 60: Peso correspondiente al jugador.
- 0C: País de nacimiento del jugador.
- 0E00 23130404414923880D0608020048: Longitud del lugar de nacimiento seguido del lugar de nacimiento.
- 0100 19: Longitud de club de debut seguida del club de debut. El editor por defecto grabará “x”.
- 0100 19: Longitud de datos de internacional del jugador seguida de los datos de internacional del jugador. El editor por defecto grabará “x”.
- 0100 19: Longitud de perfil del jugador seguida del perfil del jugador. El editor por defecto grabará “x”.
- 0100 19: Longitud de las características del jugador seguida de las características del jugador. El editor por defecto grabará “x”.
- 0100 19: Longitud del palmarés del jugador seguida del palmarés del jugador. El editor por defecto grabará “x”.
- 0100 19: Longitud la internacionalidad del jugador seguida de la internacionalidad del jugador. El editor por defecto grabará “x”.
- 0100 19: Longitud de las anécdotas del jugador seguida de las anécdotas del jugador. El editor por defecto grabará “x”.
- 0100 19: Longitud de los datos de la última temporada del jugador seguida de los datos e la última temporada del jugador. El editor por defecto grabará “x”.
- 1000 2F254D2F254D2F254D2F254D2F256C6B: Longitud de la trayectoria del jugador seguido de la trayectoria del jugador. Esta es la cadena por defecto que grabará el editor y corresponde a los valores en decimal “ND,ND,ND,ND,ND==”.
- 5654525C0D0E15191256: Medias del jugador, por este orden VE velocidad, RE resistencia, AG agresividad, CA calidad, RM remate, RG regate, PA pase, TI tiro, EN entradas y PO portero.
