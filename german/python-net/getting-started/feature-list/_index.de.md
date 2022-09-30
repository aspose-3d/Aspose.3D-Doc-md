---
title: Feature-Liste
type: docs
weight: 30
url: /de/python-net/feature-list/
---
Aspose.3D Merkmale


## **Unterstützte Plattformen**

Die Plattformen Aspose.3D für Python via .NET können unter Windows x64 oder x86 und einer Vielzahl von Linux-Distributionen mit Python 3.5 oder später verwendet werden. Es gibt zusätzliche Anforderungen an die Ziel plattform Linux:
- GCC-6 Laufzeit bibliotheken (oder später)
- Abhängigkeiten von .NET Core Runtime. Die Installation von .NET Core Runtime selbst ist NICHT erforderlich
- Für Python 3, 5-3, 7: Der Pymalloc-Build von Python wird benötigt. Die Build option -- with-pymalloc Python ist standard mäßig aktiviert. In der Regel ist der Pymalloc-Build von Python im Dateinamen mit dem Suffix m markiert.
- Libpython hat die Bibliothek Python geteilt. Die Build option-enable-shared Python ist standard mäßig deaktiviert. Einige Python-Distributionen enthalten nicht die gemeinsam genutzte libpython-Bibliothek. Bei einigen Linux-Plattformen kann die gemeinsam genutzte libpython-Bibliothek mithilfe des Paket managers installiert werden, z. B.: sudo apt-get install libpython3.7. Das häufige Problem ist, dass die libpython-Bibliothek an einem anderen Ort als der Standard-Systemsp eicher ort für gemeinsam genutzte Bibliotheken installiert ist. Das Problem kann behoben werden, indem die Build-Optionen Python verwendet werden, um alternative Bibliotheks pfade beim Kompilieren von Python festzulegen, oder indem eine symbolische Verknüpfung zur libpython-Bibliotheks datei im Systems tandard für freigegebene Bibliotheken erstellt wird. In der Regel lautet der Dateiname der gemeinsam genutzten libpython-Bibliothek libpythonX.Ym.so.1.0 für Python 3, 5-3, 7 oder libpythonX.Y.so.1.0 für Python 3,8 oder später (zum Beispiel: libpython 3,7 m.so.1.0, libpython3.9.so).
- Libgdiplus 6.0.1 oder später


## **Feature Matrix**

|**Merkmale** |` `FBX|` `Collada|` `glTF|` `glTF 2.0|` `U3D|` `PDF|` `STL|` `OBJ|` `PLY|` `3DS|` `ASE|` `X|` `3MF|` `RVM|` `Draco|
|:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |
|` `Lambert Material|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||
|` `Phong Material|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||
|` `Shader-basiertes Material|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|||||||||||||
|` `PBR Material||||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||||||||||
|Spektuläres Material ` `PBR||||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||||||||||
|` `Diffuse Textur|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|||
|` ` Fort geschrittene Textur|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||||||
|` `Polygon-Maschen|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||
|` `Triangle-basierte Maschen|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|
|` `Vertex elemente|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|
|` `NURBS Geometrien|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|||||||||||||||
|` `Param etrisierte Geometrien||||||||||||||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||
|` ` Lokale Transformation|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||
|` ` Instanierung|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||||||||
|` ` Szene graph|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||
|` `Custom immobilie|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||||||||||
|` ` Skelett|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||||||||||||
|` `Morph deformer|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||||||||||||
|` ` Immobilien animation|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||||||||||||
|` `Mesh-Kom primi erung|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|||||||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>||<p>![Todo: bild_Alt_Text](accept.png)</p><p> </p>|

