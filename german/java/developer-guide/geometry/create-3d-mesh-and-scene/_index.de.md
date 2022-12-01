---
title: Erstellen Sie 3D Mesh und Szene
type: docs
weight: 40
url: /de/java/create-3d-mesh-and-scene/
description: Ein Netz wird durch eine Reihe von Kontroll punkten und die vielen n-seitigen Polygone nach Bedarf definiert. Dieser Artikel erklärt, wie man ein Mesh definiert.
---
## **Erstellen Sie ein 3D Cube Mesh**
Eine `Mesh` wird durch eine Reihe von Kontroll punkten und die vielen n-seitigen Polygone nach Bedarf definiert. Dieser Artikel erklärt, wie man eine `Mesh` definiert.

Um eine `Mesh`-Oberfläche zu erstellen, müssen wir Steuer punkte und Polygone wie folgt definieren:

- [Definieren Sie die Kontroll punkte](/3d/de/java/create-3d-mesh-and-scene-html/)
- [Erstellen Sie Polygone mit der Klasse PolygonBuilder](/3d/de/java/create-3d-mesh-and-scene-html/)
- [Polygone erstellen](/3d/de/java/create-3d-mesh-and-scene-html/)

Hier ist ein Beispiel zum Anhängen eines Phong-Materials an den Würfel knoten:
### **Definieren Sie die Kontroll punkte**
Ein Netz besteht aus einer Reihe von Kontroll punkten im Raum und Polygonen, um die Netz oberfläche zu beschreiben. Um ein Netz zu erstellen, müssen wir die Kontroll punkte definieren:

{{% alert color="primary" %}} 

Die Kontroll punkte aller Geometrien in Aspose.3D verwenden eine homogene Koordinate, daher ist es `Vector4` anstelle von `Vector3` im Beispiel code.

{{% /alert %}} 

**Beispiel:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-DefineControlPoints.java" >}}



### **Polygone erstellen**
Die Kontroll punkte sind nicht render ierbar. Um den Würfel sichtbar zu machen, müssen wir Polygone auf jeder Seite definieren:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingCreatePolygons.java" >}}



### **Erstellen Sie Polygone mit der Klasse PolygonBuilder**
Wir können Polygon auch durch Eckpunkte mit der Klasse PolygonBuilder definieren:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingPolygonBuilder.java" >}}

Jetzt ist es fertig, um das Netz sichtbar zu machen, müssen wir einen Knoten dafür vorbereiten.
## **Wie man ein Netz trianguliert**
Triangulate Mesh ist für die Spiele industrie nützlich, da das Dreiecksnetz das einzige unterstützte Primitiv ist, das die GPU-Hardware unterstützt (nicht dreieckige Daten werden auf Treiber ebene trianguliert, was beim Echtzeit-Rendering ineffizient ist).

{{% alert color="primary" %}} 

In dieser Version haben wir die Polygone nur trianguliert, da dies für den Export von 3ds-Dateien erforderlich ist. Normalen/Uvs und andere Scheitel punkt elemente gehen während dieses Verfahrens verloren. Wir können dies in Zukunft implemen tieren.

{{% /alert %}} 

In diesem Beispiel triangulieren wir ein Mesh, indem wir die Datei FBX importieren und im Format FBX speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-TriangulateMesh.java" >}}
## **Erstellen Sie eine Cube-Szene 3D**
Dieses Thema zeigt, wie Sie der Szene 3D Mesh-Geometrie hinzufügen. Der Beispielcode platziert einen Cube und speichert die Szene 3D in den unterstützten Dateiformaten.
### **Erstellen Sie einen Würfel knoten**
Ein Knoten ist unsichtbar, aber die an den Knoten angehängte Geometrie kann gerendert werden.

{{% alert color="primary" %}} 

Das Mesh-Klassen objekt wird im Code verwendet. Wir können[Erstellen Sie ein Mesh-Klassen objekt, wie es dort erzählt wird](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh).

{{% /alert %}} 

**Beispiel:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateCubeScene.java" >}}

{{% alert color="primary" %}} 

HINWEIS: Die Entitäten, die an den Stamm knoten anges ch lossen sind, werden normaler weise in CAD/CAM-Software ignoriert. Daher müssen wir einen neuen Knoten erstellen, um die Geometrie zu rendern.

{{% /alert %}}
