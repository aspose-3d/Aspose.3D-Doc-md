---
title: Mesh in Triangle Mesh und primitive Form in Mesh konvertieren
type: docs
weight: 30
url: /de/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Mit Aspose.3D for Python via .NET API können Entwickler jedes Mesh-Objekt in ein Dreiecks netz mit benutzer definiertem Speicher layout des Scheitel punkts konvertieren. Das benutzer definierte Speicher layout des Vertex wird mithilfe der Struktur oder dynamisch durch die VertexDeclaration-Klasse in den Code beispielen definiert.
---
##  **Konvertieren Sie ein Mesh in Triangle Mesh mit benutzer definiertem Speicher layout des Vertex**
Mit [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API können Entwickler jedes Mesh-Objekt in ein Dreiecks netz mit benutzer definiertem Speicher layout des Scheitel punkts konvertieren. Das benutzer definierte Speicher layout des Vertex wird mithilfe der Struktur oder dynamisch durch die [`VertexDeclaration`](http://www.aspose.com/api/net/3d/aspose.threed.utilities/vertexdeclaration)-Klasse in den Code beispielen definiert.

{{% alert color="primary" %}}

Dieses Hilfe thema erstellt Maschen aus der Box und der Sphäre, um den Code umfassend und kurz zu halten. Entwickler können ein Netz manuell erstellen, wie in diesem Hilfe thema beschrieben: [Erstellen Sie ein 3D Cube Mesh](/3d/de/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Diese Beispiele zeigen, wie man:

- [Konvertieren Sie eine Sphere in Triangle Mesh mit benutzer definiertem Speicher layout des Scheitel punkts (definiert in der Struktur).](/3d/de/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Konvertieren Sie eine Box in Triangle Mesh mit benutzer definiertem Speicher layout des Scheitel punkts (definiert durch die VertexDeclaration-Klasse).](/3d/de/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
###  **Mesh konvertieren**
Entwickler können Mesh in Dreiecks netz konvertieren, da jede komplexe (Oberflächen-) Struktur als eine Reihe von Dreiecken dargestellt werden kann. Das Dreieck ist die atomare Geometrie. Somit wird es als Basis für fast alles verwendet.
###  **Zugriffs scheitel punkte eines Dreiecks netzes**
Entwickler können vor dem Zusammenführen auf Indizes, tatsächliche Eckpunkte, Eckpunkte und Gesamt bytes von Scheitel punkten im Speicher zugreifen.

Das folgende Beispiel konvertiert eine Kugel in ein Dreiecks netz mit benutzer definiertem Speicher layout.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.py" >}}




Das folgende Beispiel konvertiert eine Box in ein Dreiecks netz mit benutzer definiertem Speicher layout.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.py" >}}
##  **Konvertieren Sie das "Primitive" in ein "Mesh"**
Mit Aspose.3D for Python via .NET können Entwickler jedes primitive Objekt in ein Netz konvertieren. Zu den Primitiven gehören viele der grundlegend sten und am häufigsten verwendeten Objekte wie Box, Kugel, Ebene, Zylinder und Torus.

{{% alert color="primary" %}}

Jede Klasse, die eine Schnitts telle IMesh Convertible implementiert, kann beim Exportieren in ein beliebiges 3D-Dateiformat in Mesh konvertiert werden.

{{% /alert %}}
###  **Konvertieren Sie eine "Sphere" in "Mesh"**
Eine Kugel ist ein perfekt rundes geometrisches Objekt im drei dimensionalen Raum, das überall von Sport bällen bis zu Planeten im Weltraum erscheint. Verwenden wir das Sphären primitiv, um ein Netz zu erstellen.
Das folgende Code beispiel konvertiert eine Sphäre in ein Netz.

{{< highlight "python" >}}
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Sphere class
convertible = Sphere()
#  Convert a Sphere to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Eine "Box" in "Mesh" konvertieren**
Eine Box beschreibt eine Vielzahl von Behältern und Behältern zur dauerhaften Verwendung als Lagerung oder zur vorübergehen den Verwendung, häufig zum Transport von Inhalten. Verwenden wir das Box-Primitiv, um ein Netz zu erstellen. Das folgende Code beispiel konvertiert eine Box in ein Netz.

{{< highlight "python" >}}
from aspose.threed.entities import Box

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Box class
convertible = Box()
#  Convert a Box to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Konvertieren Sie eine "Plane" in "Mesh"**
Eine Ebene erstreckt sich unendlich ohne Dicke. Ein Beispiel für eine Ebene ist eine Koordinaten ebene. Lassen Sie uns das Flugzeug primitiv verwenden, um ein Netz zu erstellen. Das folgende Code beispiel konvertiert eine Ebene in ein Netz.

{{< highlight "python" >}}
from aspose.threed.entities import Plane

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Plane class
convertible = Plane()
#  Convert a Plane to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Konvertieren Sie einen "Zylinder" in "Mesh"**
Ein Zylinder ist eine der grundlegend sten krumm linigen geometrischen Formen, wobei die Oberfläche von den Punkten in einem festen Abstand von einer bestimmten geraden Linie, der Achse des Zylinders, gebildet wird. Sie ist vieler orts einsetzbar, etwa als Pfeiler vor einem Eigenheim oder als Auto antriebswelle. Lassen Sie uns das Zylinder primitiv verwenden, um ein Netz zu erstellen. Das folgende Code beispiel konvertiert einen Zylinder in ein Netz.

{{< highlight "python" >}}
from aspose.threed.entities import Cylinder

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Cylinder class
convertible = Cylinder()
#  Convert a Cylinder to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Konvertieren Sie einen "Torus" in "Mesh"**
Ein Torus ist eine Umdrehung fläche, die durch Drehen eines Kreises im drei dimensionalen Raum um eine mit dem Kreis koplanare Achse erzeugt wird. Wenn die Umdrehung achse den Kreis nicht berührt, hat die Oberfläche eine Ringform und wird als Torus der Revolution bezeichnet. Verwenden wir das Torus-Primitiv, um ein Netz zu erstellen. Das folgende Code beispiel konvertiert einen Torus in ein Netz.

{{< highlight "python" >}}
from aspose.threed.entities import Torus

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Torus class
convertible = Torus()
#  Convert a Torus to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
