---
title: Skapa 3D Mesh och Scene
type: docs
weight: 40
url: /sv/java/create-3d-mesh-and-scene/
description: En Mesh definieras av en uppsättning styrpunkter och de många n-sidig polygoner som behövs. Den här artikeln förklarar hur man definierar en Mesh.
---
##  **Skapa en 3D kubst**
En `Mesh` definieras av en uppsättning kontrollpunkter och de många polygoner som behövs. Den här artikeln förklarar hur man definierar en `Mesh`.

För att skapa en `Mesh`-yta måste vi definiera styrpunkter och polygoner på följande sätt:

- [Define the Control Points](/3d/java/create-3d-mesh-and-scene-html/)
- [Create Polygons with PolygonBuilder Class](/3d/java/create-3d-mesh-and-scene-html/)
- [Create Polygons](/3d/java/create-3d-mesh-and-scene-html/)

Här är ett exempel för att bifoga ett Phong-material till kubennoden:
###  **Definiera kontrollpunkter**
En mash består av en uppsättning styrpunkter i rymden och polygoner för att beskriva maskstytan för att skapa en mask. Vi måste definiera kontrollpunkterna:

{{% alert color="primary" %}} 

Kontrollpunkterna för alla geometrier i Aspose. 3D använd homogen koordinat, så det är `Vector4` istället för `Vector3` i exempelkoden.

{{% /alert %}} 

**Exempel:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-DefineControlPoints.java" >}}



###  **Skapa polygoner**
Kontrollpunkterna är inte utförbara, för att göra kuben synlig, måste vi definiera polygoner i varje sida:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingCreatePolygons.java" >}}



###  **Skapa polygoner med PolygonBuilder Name**
Vi kan också definiera polygon med hörn med PolygonBuilder klass:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingPolygonBuilder.java" >}}

Nu är det klart, för att göra nätverket synligt, måste vi förbereda en nod för det.
##  **Hur man kan tränga ett tåg**
Triangulera mesh är användbart för spelindustrin eftersom den trekantiga är den enda primitiva som stöds GPU-hårdvaran stöder (icke-triangulära data är triangulerad i förarnivå, som är ineffektiv i realtids rendering)

{{% alert color="primary" %}} 

I denna version vi bara triangulerade polygoner eftersom det krävs av 3ds fil export, normaler/uvs och andra vertex element går förlorade under denna förfarande, vi kan genomföra detta i framtiden.

{{% /alert %}} 

I det här exemplet triangulerar vi en mesh genom att importera FBX-fil och sparade den i FBX-format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-TriangulateMesh.java" >}}
##  **Skapa en 3D kubscene**
Detta ämne visar hur mesh-geometrin ska läggas till i 3D-scenen. Exemplets kod placerar en kub och sparar 3D scen i de filformat som stöds.
###  **Skapa en kubnod**
En nod är osynlig, men geometrin som är kopplad till noden kan renderas.

{{% alert color="primary" %}} 

Mesh-klassobjektet används i koden. Vi kan [Skapa ett Mesh-klassobjekt som berättat där.](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh).

{{% /alert %}} 

**Exempel:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateCubeScene.java" >}}

{{% alert color="primary" %}} 

OBS: De enheter som är anslutna till rotnoden ignoreras vanligtvis i CAD/CAM-programvara, så vi behöver skapa en ny nod för att göra geometrin.

{{% /alert %}}
