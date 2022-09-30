---
title: Normalen oder UV auf dem Würfel einrichten und Material zu 3D Entitäten hinzufügen
type: docs
weight: 20
url: /de/python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: So erstellen Sie Normalen oder UV-Daten auf einem Netz in Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D für Python via .NET bietet die Verwaltung von Normalen und UV auf die geometrischen Formen. Ein Netz speichert die Schlüssel eigenschaften für jeden Scheitel punkt, sind seine Position im Raum und seine Normalität, ein Vektor senkrecht zur ursprünglichen Oberfläche. Das Normale ist wichtig für die Schattierung zählt. Die Normalen sollten Einheits vektoren sein. Die meisten Netz formate unterstützen auch eine Form von UV-Koordinaten, bei denen es sich um eine separate 2D-Darstellung des "entfalteten" Netzes handelt, um zu zeigen, welcher Teil einer zwei dimensionalen Textur karte auf verschiedene Polygone des Netzes angewendet werden soll.

{{% /alert %}} {{% alert color="primary" %}}

Das Klassen objekt `Mesh` wird im Code verwendet. Wir können[Erstellen Sie ein `Mesh`-Klassenobjekt, wie es dort erzählt wird](/3d/de/python-net/create-3d-mesh-and-scene/)Und dann zeigen Sie den Knoten auf die Mesh-Geometrie durch[Erstellen einer 3D Szene](/3d/de/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Normale Vektoren erstellen**
Um ein gutes visuelles Aussehen der Beleuchtung zu haben, müssen wir Normale Informationen für jeden Scheitel punkt angeben, um bessere Details zu haben, können wir auch normale und diffuse Karte verwenden (sicher, dass Sie Schatten/spekulare Karte verwenden können), um pro Pixel normal/Farbe auszuführen. Eine Pro-Scheitel punkt-Information wie Normal-oder Scheitel punkt farbe wird durch `VertexElement` erreicht. In Aspose.3D können wir zusätzliche Informationen an Kontroll punkte/Polygon vertex/Polygon/Kante abbilden, ein Beispiel zur Definition von Normalen für den Scheitel punkt:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.py" >}}

Die 8 normalen Vektoren werden direkt 8 Kontroll punkten zugeordnet. Im nächsten Beispiel werden wir ein etwas komplexeres Szenario demonstrieren.
## **Erstellen von UV-Koordinaten**
Hier haben wir nur 4 UV-Koordinaten definiert, sie jedoch mithilfe von Indizes auf 24 Polygon scheitel punkte (6 Fläche * 4 Scheitel punkt pro Polygon) angewendet.
Die Aspose.3D bietet 5 Mapping-Modi:

- `CONTROL_POINT`-Jeder Daten wird dem Kontroll punkt der Geometrie zugeordnet.
- `POLYGON_VERTEX`-Die Daten werden dem Scheitel punkt des Polygons zugeordnet.
- `POLYGON`-Die Daten werden dem Polygon zugeordnet.
- `EDGE`-Die Daten werden auf den Rand abgebildet.
- `ALL_SAME`-Ein Daten, der der gesamten Geometrie zugeordnet ist.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupUVOnCube-SetupUVOnCube.py" >}}
## **Materialien zu 3D Objekten hinzufügen**
Aspose.3D für Python via .NET ermöglicht es Entwicklern, den Schattierung algorithmus für genaue Schattierung und Highlights zu verwenden. Der Phong verfügt über mehrere Karten eingaben, mit denen wir den Effekt auf den Knoten maskieren können. Physically Based Rendering (PBR) berücksicht igt einige physikalische Eigenschaften von Objekten. Ein solcher Ansatz bietet das Erscheinung sbild von Materialien wie in der realen Welt.
### **Phong Material mit Textur für Würfel**
Wenn die UV-Koordinaten einsatz bereit sind, können wir eine Textur auf die Oberfläche des Netzes anwenden, indem wir Material verwenden. Nur die Scheitel punkt farbe kann die Details der Oberfläche nicht beschreiben, dafür werden Materialien verwendet. Hier ist ein Beispiel zum Anhängen eines Phong-Materials an den Würfel knoten:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MaterialToCube-AddMaterialToCube.py" >}}

Wir haben die diffuse Textur abbildung und eine spiegele Farbe mit einem Glanz parameter angegeben.
### **Wenden Sie physikalisch basiertes Rendering-Material (PBR) auf eine Box an**
PBR spielt eine Schlüssel rolle für die Game Engine-Grafik mit seiner effizienten und realistischen Darstellung von Wechsel wirkungen zwischen Licht und Oberfläche durch Dämpfung der Helligkeit und Streuung von reflektiertem Licht. Entwickler können Aspose.3D API verwenden, um PBR-Material auf 3D-Objekte in einer Szene anzuwenden. In diesem Code beispiel wird ver anschaulicht, wie ein Box-Objekt erstellt und anschließend das PBR-Material angewendet wird.

**.NET, C#**

```py
import aspose.threed as a3d
# initialize a scene

scene = a3d.Scene()

# initialize PBR material object

mat = a3d.shading.PbrMaterial()

# an almost metal material

mat.metallic_factor = 0.9

# material surface is very rough

mat.roughness_factor = 0.9;

# create a box to which the material will be applied

boxNode = scene.root_node.create_child_node("box", a3d.entities.Box())

boxNode.material = mat

# save 3d scene into STL format

scene.save("PBR_Material_Box_Out.stl", a3d.FileFormat.STLASCII)

```
