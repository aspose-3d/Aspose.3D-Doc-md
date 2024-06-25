---
title: Feature-Liste
type: docs
weight: 30
url: /de/python-net/feature-list/
---
Aspose.3D Funktionen


##  **Unterstützte Plattformen**

Die Plattformen Aspose.3D for Python via .NET können auf Windows x64 oder x86 und einer Vielzahl von Linux-Distributionen mit Python 3.5 oder höher verwendet werden. Es gibt zusätzliche Anforderungen an die Ziel-Linux-Plattform:
- GCC-6 Laufzeit bibliotheken (oder später)
- Abhängigkeiten von .NET Core Runtime. Die Installation von .NET Core Runtime selbst ist NICHT erforderlich
- Für Python 3.5-3.7: Der Pymalloc-Build von Python wird benötigt. Die Build option -- with-pymalloc Python ist standard mäßig aktiviert. In der Regel wird der Pymalloc-Build von Python im Dateinamen mit dem Suffix m markiert.
- Libpython teilte Python Bibliothek. Die Build-Option-enable-shared Python ist standard mäßig deaktiviert. Einige Python-Distributionen enthalten nicht die gemeinsam genutzte libpython-Bibliothek. Bei einigen Linux-Plattformen kann die gemeinsam genutzte libpython-Bibliothek mithilfe des Paket managers installiert werden, z. B.: sudo apt-get install libpython3.7. Das häufige Problem ist, dass die libpython-Bibliothek an einem anderen Ort als der Standard-Systemsp eicher ort für gemeinsam genutzte Bibliotheken installiert ist. Das Problem kann behoben werden, indem Sie die Build-Optionen für Python verwenden, um alternative Bibliotheks pfade beim Kompilieren von Python festzulegen, oder indem Sie eine symbolische Verknüpfung zur libpython-Bibliotheks datei im Systems tandard für freigegebene Bibliotheken erstellen. In der Regel lautet der Dateiname der gemeinsam genutzten libpython-Bibliothek libpythonX.Ym.so.1.0 für Python 3, 5-3, 7 oder libpythonX.Y.so.1.0 für Python 3,8 oder höher (zum Beispiel: libpython 3,7 m.so.1.0, libpython3.9.so).
- Libgdiplus 6.0.1 oder später


##  **Feature Matrix**

|**Merkmale** |` `FBX|` `Collada|` `glTF|` `glTF 2.0|` `U3D|` `PDF|` `STL|` `OBJ|` `PLY|` `3DS|` `ASE|` `X|` `3MF|` `RVM|` `Draco|
| :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- |
|` `Lambert Material|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | |
|` `Phong Material|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | |
|` `Shader-basiertes Material|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | |
|` `PBR-Material| | | |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | |
|` `PBR-Spekulares Material| | | |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | |
|` `Diffuse Textur|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | |
|` ` Erweiterte Textur|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | | | | | |
|` `Polygon-Maschen|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | | | |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | | | |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |
|` ` Dreieck-basierte Maschen|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|
|` `Vertex-Elemente|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|
|` `NURBS Geometrien|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | | |
|` `Param etrisierte Geometrien| | | | | | | | | | | | | |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |
|` ` Lokale Transformation|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |
|` ` Instanierung|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | | | | | | | |
|` ` Szenen diagramm|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |
|` ` Benutzer definierte Eigenschaft|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | |
|` ` Skelett|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | |
|` `Morph deformer|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | |
|` ` Immobilien animation|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | |
|` ` Netz kompression|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| | | | | | |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>| |<p>! [Todo: image_alt_text](accept.png)</p><p> </p>|

