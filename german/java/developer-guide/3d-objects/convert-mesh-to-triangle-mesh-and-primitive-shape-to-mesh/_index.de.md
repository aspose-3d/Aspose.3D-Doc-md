---
title: Mesh in Triangle Mesh und primitive Form in Mesh konvertieren
type: docs
weight: 20
url: /de/java/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for Java API bietet Unterstützung für die Konvertierung von Mesh in Triangle Mesh mit benutzer definiertem Speicher layout des Scheitel punkts. Das benutzer definierte Speicher layout des Vertex wird dynamisch durch die VertexDeclaration-Klasse in den Code beispielen definiert.
---
##  **Konvertieren Sie Mesh in Triangle Mesh mit benutzer definiertem Speicher layout von Vertex**
Aspose.3D for Java API bietet Unterstützung für die Konvertierung von Mesh in Triangle Mesh mit benutzer definiertem Speicher layout des Scheitel punkts. Das benutzer definierte Speicher layout des Vertex wird dynamisch durch die `VertexDeclaration`-Klasse in den Code beispielen definiert.

{{% alert color="primary" %}}

Dieses Hilfe thema erstellt Maschen aus der Box und der Sphäre, um den Code umfassend und kurz zu halten. Entwickler können ein Netz manuell erstellen, wie in diesem Hilfe thema beschrieben: [3D Cube Mesh erstellen](/3d/de/java/create-3d-mesh-and-scene/).

{{% /alert %}}

Entwickler können Mesh in Dreiecks netz konvertieren, da jede komplexe (Oberflächen-) Struktur als eine Reihe von Dreiecken dargestellt werden kann. Das Dreieck ist die atomare Geometrie. Somit wird es als Basis für fast alles verwendet. In diesem Code beispiel wird eine Box in ein Dreiecks netz mit benutzer definiertem Speicher layout konvertiert.



{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize Node class object
Node cubeNode = new Node("box");
// Get mesh of the Box
Mesh box = (new Box()).toMesh();
// Create a customized vertex layout
VertexDeclaration vd = new VertexDeclaration();
VertexField position = vd.addField(VertexFieldDataType.F_VECTOR4, VertexFieldSemantic.POSITION);
vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.NORMAL);
// Get a triangle mesh
TriMesh triMesh = TriMesh.fromMesh(box);
// ExEnd:ConvertBoxMeshtoTriangleMeshCustomMemoryLayout
// Point node to the Mesh geometry
cubeNode.setEntity(box);
// Add Node to a scene
scene.getRootNode().getChildNodes().add(cubeNode);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir() + RunExamples.getOutputFilePath("BoxToTriangleMeshCustomMemoryLayoutScene.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}
##  **Primitive Form zu Mesh konvertieren**
Aspose.3D for Java API unterstützt die Umwandlung einer beliebigen primitiven Form in Mesh. Zu den primitiven Formen gehören die meisten grundlegenden und verwendeten Objekte wie Box, Kugel, Ebene, Zylinder und Torus.

{{% alert color="primary" %}}

Jede Klasse, die eine Schnitts telle IMesh Convertible implementiert, kann beim Exportieren in ein beliebiges 3D-Dateiformat in Mesh konvertiert werden.

{{% /alert %}}
###  **Konvertieren Sie Primitive zu Ineinander greifen**
Eine Kugel ist ein perfekt rundes geometrisches Objekt im drei dimensionalen Raum, das überall von Sport bällen bis zu Planeten im Weltraum erscheint. Verwenden wir das Sphären primitiv, um ein Netz zu erstellen.
Das folgende Code beispiel konvertiert eine Sphäre in ein Netz.

{{< highlight "java" >}}
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
// Convert a Sphere to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Box zu Mesh konvertieren**
Eine Box beschreibt eine Vielzahl von Behältern und Behältern zur dauerhaften Verwendung als Lagerung oder zur vorübergehen den Verwendung, häufig zum Transport von Inhalten. Verwenden wir das Box-Primitiv, um ein Netz zu erstellen. Das folgende Code beispiel konvertiert eine Box in ein Netz.

{{< highlight "java" >}}
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Konvertieren Sie ein Flugzeug in ein Netz**
Eine Ebene erstreckt sich unendlich ohne Dicke. Ein Beispiel für eine Ebene ist eine Koordinaten ebene. Lassen Sie uns das Flugzeug primitiv verwenden, um ein Netz zu erstellen. Das folgende Code beispiel konvertiert eine Ebene in ein Netz.

{{< highlight "java" >}}
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
// Convert a Plane to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Konvertieren Sie einen Zylinder in ein Netz**
Ein Zylinder ist eine der grundlegend sten krumm linigen geometrischen Formen, wobei die Oberfläche von den Punkten in einem festen Abstand von einer bestimmten geraden Linie, der Achse des Zylinders, gebildet wird. Sie ist vieler orts einsetzbar, etwa als Pfeiler vor einem Eigenheim oder als Auto antriebswelle. Lassen Sie uns das Zylinder primitiv verwenden, um ein Netz zu erstellen. Das folgende Code beispiel konvertiert einen Zylinder in ein Netz.

{{< highlight "java" >}}
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
// Convert a Cylinder to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Einen Torus in Mesh umwandeln**
Ein Torus ist eine Umdrehung fläche, die durch Drehen eines Kreises im drei dimensionalen Raum um eine mit dem Kreis koplanare Achse erzeugt wird. Wenn die Umdrehung achse den Kreis nicht berührt, hat die Oberfläche eine Ringform und wird als Torus der Revolution bezeichnet. Verwenden wir das Torus-Primitiv, um ein Netz zu erstellen. Das folgende Code beispiel konvertiert einen Torus in ein Netz.

{{< highlight "java" >}}
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
// Convert a Torus to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
