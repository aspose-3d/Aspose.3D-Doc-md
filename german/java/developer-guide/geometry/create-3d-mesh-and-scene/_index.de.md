---
title: 3D Mesh und Szene erstellen
type: docs
weight: 40
url: /de/java/create-3d-mesh-and-scene/
description: Ein Netz wird durch eine Reihe von Kontroll punkten und die vielen n-seitigen Polygone nach Bedarf definiert. Dieser Artikel erklärt, wie man ein Mesh definiert.
---
##  **Erstellen Sie ein 3D Cube Mesh**
A `Mesh` wird durch eine Reihe von Kontroll punkten und die vielen n-seitigen Polygone nach Bedarf definiert. In diesem Artikel wird erläutert, wie ein `Mesh` definiert wird.

Um eine `Mesh`-Oberfläche zu erstellen, müssen wir Steuer punkte und Polygone wie folgt definieren:

- [Definieren Sie die Kontroll punkte](/3d/de/java/create-3d-mesh-and-scene-html/)
- [Erstellen Sie Polygone mit der PolygonBuilder-Klasse](/3d/de/java/create-3d-mesh-and-scene-html/)
- [Polygone erstellen](/3d/de/java/create-3d-mesh-and-scene-html/)

Hier ist ein Beispiel zum Anhängen eines Phong-Materials an den Würfel knoten:
###  **Definieren Sie die Kontroll punkte**
Ein Netz besteht aus einer Reihe von Kontroll punkten im Raum und Polygonen, um die Netz oberfläche zu beschreiben. Um ein Netz zu erstellen, müssen wir die Kontroll punkte definieren:

{{% alert color="primary" %}} 

Die Kontroll punkte aller Geometrien in Aspose.3D verwenden eine homogene Koordinate, also `Vector4` statt `Vector3` im Beispiel code.

{{% /alert %}} 

**Beispiel:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-DefineControlPoints.java" >}}



###  **Polygone erstellen**
Die Kontroll punkte sind nicht render ierbar. Um den Würfel sichtbar zu machen, müssen wir Polygone auf jeder Seite definieren:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingCreatePolygons.java" >}}



###  **Erstellen Sie Polygone mit der PolygonBuilder-Klasse**
Wir können Polygon auch durch Eckpunkte mit der PolygonBuilder-Klasse definieren:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingPolygonBuilder.java" >}}

Jetzt ist es fertig, um das Netz sichtbar zu machen, müssen wir einen Knoten dafür vorbereiten.
##  **Wie man ein Netz trianguliert**
Triangulate Mesh ist für die Spiele industrie nützlich, da das Dreiecksnetz das einzige unterstützte Primitiv ist, das die GPU-Hardware unterstützt (nicht dreieckige Daten werden auf Treiber ebene trianguliert, was beim Echtzeit-Rendering ineffizient ist).

{{% alert color="primary" %}} 

In dieser Version haben wir die Polygone nur trianguliert, da dies für den Export von 3ds-Dateien erforderlich ist. Normalen/Uvs und andere Scheitel punkt elemente gehen während dieses Verfahrens verloren. Wir können dies in Zukunft implemen tieren.

{{% /alert %}} 

In diesem Beispiel triangulieren wir ein Mesh, indem wir eine FBX-Datei importieren und im FBX-Format speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-TriangulateMesh.java" >}}
##  **Erstellen Sie eine 3D Cube-Szene**
Dieses Thema zeigt, wie Mesh-Geometrie zur 3D-Szene hinzugefügt wird. Der Beispielcode platziert einen Cube und speichert 3D Szene in den unterstützten Dateiformaten.
###  **Erstellen Sie einen Würfel knoten**
Ein Knoten ist unsichtbar, aber die an den Knoten angehängte Geometrie kann gerendert werden.

{{% alert color="primary" %}} 

Das Mesh-Klassen objekt wird im Code verwendet. Wir können [Erstellen Sie ein Mesh-Klassen objekt, wie es dort erzählt wird](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh).

{{% /alert %}} 

**Beispiel:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateCubeScene.java" >}}

{{% alert color="primary" %}} 

HINWEIS: Die an den Stamm knoten angehängten Entitäten werden normaler weise in CAD/CAM-Softwares ignoriert. Daher müssen wir einen neuen Knoten erstellen, um die Geometrie zu rendern.

{{% /alert %}}
