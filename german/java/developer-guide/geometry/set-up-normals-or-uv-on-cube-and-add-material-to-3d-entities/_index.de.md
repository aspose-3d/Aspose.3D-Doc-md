---
title: Normalen oder UV-auf Cube einrichten und Material zu 3D Entitäten hinzufügen
type: docs
weight: 60
url: /de/java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java bietet Normalen und UV auf die geometrischen Formen zu verwalten. Ein Netz speichert die Schlüssel eigenschaften für jeden Scheitel punkt, jede Position im Raum und seine Normalität, der als Vektor senkrecht zur ursprünglichen Oberfläche bezeichnet wird. Die Normalität ist für die Schattierung zählungen wichtig und sollte ein Einheits vektor sein. Die meisten Netz formate unterstützen auch eine Form von UV-Koordinaten, bei denen es sich um eine separate 2D-Darstellung des "entfalteten" Netzes handelt, um zu zeigen, welcher Teil einer zwei dimensionalen Textur karte auf verschiedene Polygone des Netzes angewendet werden soll.
---
{{% alert color="primary" %}}

Aspose.3D for Java bietet Normalen und UV auf die geometrischen Formen zu verwalten. Ein Netz speichert die Schlüssel eigenschaften für jeden Scheitel punkt, jede Position im Raum und seine Normalität, der als Vektor senkrecht zur ursprünglichen Oberfläche bezeichnet wird. Die Normalität ist für die Schattierung zählungen wichtig und sollte ein Einheits vektor sein. Die meisten Netz formate unterstützen auch eine Form von UV-Koordinaten, bei denen es sich um eine separate 2D-Darstellung des "entfalteten" Netzes handelt, um zu zeigen, welcher Teil einer zwei dimensionalen Textur karte auf verschiedene Polygone des Netzes angewendet werden soll.

{{% /alert %}} {{% alert color="primary" %}}

Das `Mesh`-Klassen objekt wird im Code verwendet. Wir können [Erstellen Sie ein Mesh-Klassen objekt, wie hier erzählt](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) und dann den Knoten auf die Mesh-Geometrie zeigen, indem wir eine 3D-Szene erstellen.

{{% /alert %}}
##  **Normale Vektoren erstellen**
Um ein gutes visuelles Aussehen der Beleuchtung zu haben, müssen wir normale Informationen für jeden Scheitel punkt angeben. Um die besseren Details zu erhalten, können wir auch eine normale und diffuse Karte verwenden (verwenden Sie Schatten/spiegelnde Karte), um Normal/Farbe pro Pixel auszuführen. Eine Pro-Vertex-Information wie Normal-oder Scheitel punkt farbe wird durch Vertex Element erreicht. In Aspose.3D können wir zusätzliche Informationen an Kontroll punkte/Polygon vertex/Polygon/Kante abbilden, ein Beispiel, um Normalen für Scheitel punkt zu definieren:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupNormalsOnCube.java" >}}


Die 8 normalen Vektoren werden direkt 8 Kontroll punkten zugeordnet. Im nächsten Beispiel werden wir ein etwas komplexeres Szenario demonstrieren.
##  **Erstellen von UV-Koordinaten**
Hier haben wir nur 4 UV-Koordinaten definiert, sie jedoch mithilfe von Indizes auf 24 Polygon scheitel punkte (6 Fläche * 4 Scheitel punkt pro Polygon) angewendet.
Die Aspose.3D bietet 5 Mapping-Modi:

- **Kontroll punkt**-Jede Daten wird dem Kontroll punkt der Geometrie zugeordnet.
- **Polygon vertex**-Die Daten werden dem Scheitel punkt des Polygons zugeordnet.
- **Polygon**-Die Daten werden dem Polygon zugeordnet.
- **Rand**-Die Daten werden auf den Rand abgebildet.
- **AllSame**-Eine Daten, die der gesamten Geometrie zugeordnet sind.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupUVOnCube.java" >}}
##  **Materialien zu 3D Objekten hinzufügen**
Aspose.3D for Java ermöglicht es Entwicklern, Shading-Algorithmus für genaue Schattierung und Highlights zu verwenden. Der Phong verfügt über mehrere Karten eingaben, mit denen wir den Effekt auf den Knoten maskieren können. Physically Based Rendering (PBR) berücksicht igt einige physikalische Eigenschaften von Objekten. Ein solcher Ansatz bietet das Erscheinung sbild von Materialien wie in der realen Welt.
###  **Phong Material mit Textur für Würfel**
Wenn die UV-Koordinaten einsatz bereit sind, können wir eine Textur auf die Oberfläche des Netzes anwenden, indem wir Material verwenden. Nur die Scheitel punkt farbe kann die Details der Oberfläche nicht beschreiben, dafür werden Materialien verwendet. Hier ist ein Beispiel zum Anhängen eines Phong-Materials an den Würfel knoten:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddMaterialToCube.java" >}}


Wir haben die diffuse Textur abbildung und eine spiegele Farbe mit einem Glanz parameter angegeben.
###  **Wenden Sie physikalisch basiertes Rendering-Material (PBR) auf eine Box an**
PBR spielt eine Schlüssel rolle für die Game Engine-Grafik mit seiner effizienten und realistischen Darstellung von Wechsel wirkungen zwischen Licht und Oberfläche durch Dämpfung der Helligkeit und Streuung von reflektiertem Licht. Entwickler können Aspose.3D API verwenden, um PBR-Material auf 3D-Objekte in einer Szene anzuwenden. In diesem Code beispiel wird ver anschaulicht, wie ein Box-Objekt erstellt und anschließend das PBR-Material angewendet wird.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ApplyPBRMaterialToBox.java" >}}
