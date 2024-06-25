---
title: Triangulation eines einfachen Polygons
type: docs
weight: 30
url: /de/python-net/triangulation-of-a-simple-polygon/
description: Mit Aspose.3D for Python via .NET API können Entwickler ein einfaches Polygon triangulieren. Jedes Polygon kann in Dreiecke unterteilt werden. Alle Operationen und Berechnungen für Dreiecke können stückweise auf das Polygon angewendet werden.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API können Entwickler ein einfaches Polygon triangulieren. Jedes Polygon kann in Dreiecke unterteilt werden. Alle Operationen und Berechnungen für Dreiecke können stückweise auf das Polygon angewendet werden.

{{% /alert %}}
##  **Ein Polygon triangulieren**
Entwickler können Eckpunkte aus einem Polygon bereich auswählen und dann Dreiecke bilden, indem sie die Triangulate-Methode der [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier)-Klasse aufrufen, wobei jede der Formen V{1}, V{i-1}, V{i} mit dem Index i von 3 bis n. Die Klassen `Vertex` und `PolygonCanvas` in der Datei `Triangulate/PolygonCanvas.py` unter der Demo-Anwendung (Name: Triangulat) demonstrieren die Art und Weise, ein Polygon mit Aspose.3D API zu triangulieren.

{{% alert color="primary" %}}

Wir haben ein Demo-Projekt vorbereitet. Bitte beziehen Sie sich auf [Diese URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/Demos).

{{% /alert %}}
###  **Programmier probe für Triangulation**
In diesem Code beispiel werden Scheitel punkte aus einem Polygon bereich ausgewählt und dann ein Algorithmus angewendet, um Dreiecke zu erstellen. Sie können das komplette Arbeits projekt dieses Beispiels von [Hier](https://github.com/aspose-3d/Aspose.3D-for-.NET/) herunter laden.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "TriangulationSimplePolygon-Triangulate-PolygonCanvas-TriangulationofaSimplePolygon.py" >}}
