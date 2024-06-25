---
title: Funktionslista
type: docs
weight: 30
url: /sv/python-net/feature-list/
---
Aspose.3D Funktioner


##  **Plattformar som stöds**

Plattformarna Aspose.3D for Python via .NET kan användas på Windows x64 eller x86 och ett brett utbud av Linuxdistributioner med Python 3.5 eller senare installerade. Det finns ytterligare krav på målplattformen Linux:
- GCC-6 körtidsbibliotek (eller senare)
- Beroenden för .NET Core Runtime. Installera .NET kärnan körning är inte nödvändigt
- För Python 3.5-3.7: Pymalloc-byggnaden av Python behövs. Alternativet för att bygga -- withh-pymalloc Python är aktiverat som standard. Typiskt är pymalloc-byggnaden av Python markerat med m sufix i filnamnet.
- libpython shared Python library. The --enable-shared Python build option is disabled by default, some Python distributions do not contain the libpython shared library. For some linux platforms, the libpython shared library can be installed using the package manager, for example: sudo apt-get install libpython3.7. The common issue is that libpython library is installed in a different location than the standard system location for shared libraries. The issue can be fixed by using the Python build options to set alternate library paths when compiling Python, or fixed by creating a symbolic link to the libpython library file in the system standard location for shared libraries. Typically, the libpython shared library file name is libpythonX.Ym.so.1.0 for Python 3.5-3.7, or libpythonX.Y.so.1.0 for Python 3.8 or later (for example: libpython3.7m.so.1.0, libpython3.9.so.1.0).
- Libgdiplus 6. 0. 1 eller senare


##  **Funktionsmatris**

|**Egenskaper** |` `FBX |` `Collada |` `glTF |` `glTF 2.0 |` `U3D |` `PDF |` `STL |` `OBJ |` `PLY |` `3DS |` `ASE |` `X|` `3MF |` `RVM |` `Draco |
| :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- |
|` `Lambert MaterialComment|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | |
|` ` Phong|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | |
|` ` Material baserat på skådarer|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | |
|` `PBR- material:| | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | |
|` `PBR Specifikat| | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | |
|` `Diffuse texturComment|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | |
|` `Avancerad texturName|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | |
|` `Polygon mashes|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |
|` ` Triangle-baserade mashes|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|
|` ` Vertex elementer|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | |<p>![todo:image_alt_text](accept.png)</p><p> </p>|
|` `NURBS geometries |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | | |
|` `Parameterized geometries| | | | | | | | | | | | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |
|` `Lokal transformation|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |
|` `Instantering|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | |
|` ` Scene graf|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |
|` `Centifierad egenskap|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | |
|` `Skelett|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | |
|` `Morph deformare|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | |
|` ` Innehållsansvarig|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | |
|` ` Meesh komprimering|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|

