---
title: Triangulering av en enkel polygon
type: docs
weight: 30
url: /sv/net/triangulation-of-a-simple-polygon/
description: Genom att använda Aspose.3D for .NET API, kan utvecklare triangulera en enkel polygon. Alla polygon kan delas upp i trianglar. Alla åtgärder och beräkningar för trianglar kan delvis appliceras på polygonen.
---
{{% alert color="primary" %}}

Med [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API kan utvecklare triangulera en enkel polygon. Alla polygon kan delas upp i trianglar. Alla åtgärder och beräkningar för trianglar kan delvis appliceras på polygonen.

{{% /alert %}}
##  **Triangulera en polygon**
Utvecklare kan välja hörn från ett polygonområde och därefter bilda trianglar genom att ringa `Triangulate`-metoden för [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) klassen, Var och en av blanketten V{1}, V{i-1}, V{i} med indexet i från 3 till n. `Vertex` och `PolygonCanvas` klasser i `Triangulate/PolygonCanvas.cs`- filen under demoprogrammet (namn: Triangulate) visar sättet att triangulera en polygon med Aspose. 3D API.

{{% alert color="primary" %}}

Vi har förberett ett demoprojekt. Se [Webbadressen](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/Demos).

{{% /alert %}}
###  **Programmeringsprov för triangulering**
Detta kodexempel plockar hörn från ett polygonområde, och använder sedan en algoritm för att skapa trianglar. Du kan ladda ner komplett arbetsprojekt med detta exempel från [Här](https://github.com/aspose-3d/Aspose.3D-for-.NET/).

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TriangulationSimplePolygon-Triangulate-PolygonCanvas-TriangulationofaSimplePolygon.cs" >}}
