---
title: Skapa 3D Mesh och Scene
type: docs
weight: 10
url: /sv/python-net/create-3d-mesh-and-scene/
description: En Mesh definieras av en uppsättning styrpunkter och de många n-sidig polygoner som behövs. Den här artikeln förklarar hur man definierar en Mesh.
---
##  **Skapa en 3D kubst**
En [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) definieras av en uppsättning kontrollpunkter och de många polygoner som behövs. Den här artikeln förklarar hur man definierar en Mesh.

För att skapa en Mesh yta måste vi definiera styrpunkter och polygoner enligt följande:

- [Define the Control Points](/3d/python-net/create-3d-mesh-and-scene/)
- [Create Polygons with PolygonBuilder Class](/3d/python-net/create-3d-mesh-and-scene/)
- [Create Polygons](/3d/python-net/create-3d-mesh-and-scene/)

Här är ett exempel för att bifoga ett Phong-material till kubennoden:
###  **Definiera kontrollpunkter**
En mash består av en uppsättning styrpunkter i rymden och polygoner för att beskriva maskstytan för att skapa en mask. Vi måste definiera kontrollpunkterna:

{{% alert color="primary" %}}

Kontrollpunkterna för alla geometrier i Aspose. 3D använd homogen koordinat, så det är `Vector4` istället för `Vector3` i exempelkoden.

{{% /alert %}}

**Exempel:**

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-DefineControlPoints.py" >}}


###  **Skapa polygoner**
Kontrollpunkterna är inte utförbara, för att göra kuben synlig, måste vi definiera polygoner i varje sida:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-CreateMeshUsingCreatePolygons.py" >}}


###  **Skapa polygoner med PolygonBuilder Name**
Vi kan också definiera polygon med hörn med `PolygonBuilder` klass:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-CreateMeshUsingPolygonBuilder.py" >}}

Nu är det klart, för att göra nätverket synligt, måste vi förbereda en nod för det.
##  **Hur man kan tränga ett tåg**
Triangulera mesh är användbart för spelindustrin eftersom den trekantiga är den enda primitiva som stöds GPU-hårdvaran stöder (icke-triangulära data är triangulerad i förarnivå, som är ineffektiv i realtids rendering)

{{% alert color="primary" %}}

I denna version vi bara triangulerade polygoner eftersom det krävs av 3ds fil export, normaler/uvs och andra vertex element går förlorade under denna förfarande, vi kan genomföra detta i framtiden.

{{% /alert %}}

I det här exemplet triangulerar vi en mesh genom att importera FBX-fil och sparade den i FBX-format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.py" >}}
##  **Skapa en 3D kubscene**
Detta ämne visar hur mesh-geometrin ska läggas till i 3D-scenen. Exemplets kod placerar en kub och sparar 3D scen i de filformat som stöds.
###  **Skapa en kubnod**
En nod är osynlig, men geometrin som är kopplad till noden kan renderas.

{{% alert color="primary" %}}

Mesh-klassobjektet används i koden. Vi kan [Skapa ett klassobjekt `Mesh` som berättat där.](https://docs.aspose.com/3d/python-net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Exempel**

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-CubeScene-CreateCubeScene.py" >}}

{{% alert color="primary" %}}

OBS: De enheter som är anslutna till rotnoden ignoreras vanligtvis i CAD/CAM-programvara, så vi behöver skapa en ny nod för att göra geometrin.

{{% /alert %}}
