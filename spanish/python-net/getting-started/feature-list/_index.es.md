---
title: Lista de características
type: docs
weight: 30
url: /es/python-net/feature-list/
---
Aspose.3D Características


## **Plataformas soportadas**

Las plataformas Aspose.3D para Python via .NET se pueden utilizar en Windowsx64 o x86 y una amplia gama de distribuciones Linux con Python instalado 3,5 o posterior. Hay requisitos adicionales para la plataforma objetivo Linux:
- GCC-6 bibliotecas en tiempo de ejecución (o posteriores)
- Dependencias de .NET Core Runtime. La instalación de .NET Core Runtime en sí NO es necesaria
- Para Python 3.5-3.7: Se necesita la construcción pymalloc de Python. La opción de compilación -- with-pymalloc Python está activada por defecto. Por lo general, la construcción de pymalloc de Python está marcada con el sufijo m en el nombre de archivo.
- Libpython compartió la biblioteca Python. La opción de compilación -- enable-shared Python está deshabilitada de forma predeterminada, algunas distribuciones Python no contienen la biblioteca compartida libpython. Para algunas plataformas linux, la biblioteca compartida libpython se puede instalar usando el administrador de paquetes, por ejemplo: sudo apt-get install libpython3.7. El problema común es que la biblioteca libpython se instala en una ubicación diferente a la ubicación estándar del sistema para las bibliotecas compartidas. El problema se puede solucionar utilizando las opciones de compilación Python para establecer rutas de biblioteca alternativas al compilar Python, o arregladas creando un enlace simbólico al archivo de biblioteca libpython en la ubicación estándar del sistema para bibliotecas compartidas. Normalmente, el nombre del archivo de la biblioteca compartida libpython es libpythonX.Ym.so.1.0 para Python 3.5-3.7, o libpythonX.Y.so.1.0 para Python 3,8 o posterior (por ejemplo: libpython3.7m.so.1.0, libpython3.9.so. 1,0).
- Libgdiplus 6.0.1 o posterior


## **Matriz de características**

|**Características** |` `FBX|` `Collada|` `glTF|` `glTF 2,0|` `U3D|` `PDF|` `STL|` `OBJ|` `PLY|` `3DS|` `ASE|` `X|` `3MF|` `RVM|` `Draco|
|:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |
|` `Lambert Material|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||
|` `Phong Material|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||
|` `Material basado en Shader|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|||||||||||||
|` `PBR Material||||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||||||||||
|Material especular ` `PBR||||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||||||||||
|` ` Textura difusa|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|||
|` ` Textura avanzada|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||||||
|` ` Mallas de polígono|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||
|` `Mallas a base de Triangle|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|
|` ` Elementos de vértice|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|
|` ` geometrías NURBS|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|||||||||||||||
|` ` Geometrías parametrizadas||||||||||||||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||
|` ` Transformación local|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||
|` `Instancing|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||||||||
|` ` Escena gráfica|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||
|` ` Propiedad personalizada|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||||||||||
|` ` Esqueleto|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||||||||||||
|` `Morph deformador|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||||||||||||
|` ` animación de la propiedad|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||||||||||||
|` ` Compresión de malla|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|||||||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>||<p>![Todo: imagen_Alt_Texto](accept.png)</p><p> </p>|

