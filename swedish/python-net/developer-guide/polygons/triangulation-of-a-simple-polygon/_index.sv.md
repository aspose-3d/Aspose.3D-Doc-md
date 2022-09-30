---
title: Triangulering av en enkel polygon
type: docs
weight: 30
url: /sv/python-net/triangulation-of-a-simple-polygon/
description: Med Aspose.3D för Python via .NET API kan utvecklare triangulera en enkel polygon. Alla polygon kan delas upp i trianglar. Alla åtgärder och beräkningar för trianglar kan delvis appliceras på polygonen.
---
{{% alert color="primary" %}}

Användning[Aspose.3D för Python via .NET](https://products.aspose.com/3d/python-net/)API, utvecklare kan triangulera en enkel polygon. Alla polygon kan delas upp i trianglar. Alla åtgärder och beräkningar för trianglar kan delvis appliceras på polygonen.

{{% /alert %}}
## **Triangulera en polygon**
Utvecklare kan plocka hörn från ett polygonområde, och sedan bilda trianglar genom att kalla Triangulate metod i klassen [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier), var och en av formen V{1}, V{i} med indexet i går från 3 till n. `Vertex` och `PolygonCanvas` klasserna i filen `Triangulate/PolygonCanvas.py` under demoapplikationen (namn: Triangulate) visar sättet att triangulera en polygon med hjälp av Aspose.3D API.

{{% alert color="primary" %}}

Vi har förberett ett demoprojekt. Se med[Webbadressen](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/Demos).

{{% /alert %}}
### **Programmeringsprov för triangulering**
Detta kodexempel plockar hörn från ett polygonområde, och använder sedan en algoritm för att skapa trianglar. Du kan ladda ner komplett arbetsprojekt av detta exempel från[Här](https://github.com/aspose-3d/Aspose.3D-for-.NET/).

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "TriangulationSimplePolygon-Triangulate-PolygonCanvas-TriangulationofaSimplePolygon.py" >}}
