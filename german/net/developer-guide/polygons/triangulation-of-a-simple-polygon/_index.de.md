---
title: Triangulation eines einfachen Polygons
type: docs
weight: 30
url: /de/net/triangulation-of-a-simple-polygon/
description: Mithilfe von Aspose.3D for .NET APIkönnen Entwickler ein einfaches Polygon triangulieren. Jedes Polygon kann in Dreiecke unterteilt werden. Alle Operationen und Berechnungen für Dreiecke können stückweise auf das Polygon angewendet werden.
---
{{% alert color="primary" %}}

Verwendung[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API können Entwickler ein einfaches Polygon triangulieren. Jedes Polygon kann in Dreiecke unterteilt werden. Alle Operationen und Berechnungen für Dreiecke können stückweise auf das Polygon angewendet werden.

{{% /alert %}}
## **Ein Polygon triangulieren**
Entwickler können Eckpunkte aus einem Polygon bereich auswählen und dann Dreiecke bilden, indem sie die Methode `Triangulate` der Klasse [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) aufrufen, wobei jede der Form V{1}, V{i-1}, V{i}, wobei der Index i von 3 nach n geht. Die Klassen `Vertex` und `PolygonCanvas` in der Datei `Triangulate/PolygonCanvas.cs` unter der Demo-Anwendung (Name: Triangulat) demonstriert die Art und Weise, ein Polygon unter Verwendung von Aspose.3D API zu triangulieren.

{{% alert color="primary" %}}

Wir haben ein Demo-Projekt vorbereitet. Bitte beziehen Sie sich auf[Diese URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/Demos).

{{% /alert %}}
### **Programmier probe für Triangulation**
In diesem Code beispiel werden Scheitel punkte aus einem Polygon bereich ausgewählt und dann ein Algorithmus angewendet, um Dreiecke zu erstellen. Sie können das komplette Arbeits projekt dieses Beispiels von herunter laden[Hier](https://github.com/aspose-3d/Aspose.3D-for-.NET/).

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TriangulationSimplePolygon-Triangulate-PolygonCanvas-TriangulationofaSimplePolygon.cs" >}}
