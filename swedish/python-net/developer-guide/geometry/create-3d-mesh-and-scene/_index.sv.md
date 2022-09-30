---
title: Skapa 3D Mesh och Scene
type: docs
weight: 10
url: /sv/python-net/create-3d-mesh-and-scene/
description: En Mesh definieras av en uppsättning styrpunkter och de många n-sidig polygoner som behövs. Den här artikeln förklarar hur man definierar en Mesh.
---
## **Skapa en 3D Cube mesh**
En [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) definieras av en uppsättning styrpunkter och de många n-sidig polygoner som behövs. Den här artikeln förklarar hur man definierar en Mesh.

För att skapa en Mesh yta måste vi definiera styrpunkter och polygoner enligt följande:

- [Definiera kontrollpunkter](/3d/sv/python-net/create-3d-mesh-and-scene/)
- [Skapa polygoner med PolygonBuilder klass](/3d/sv/python-net/create-3d-mesh-and-scene/)
- [Skapa polygoner](/3d/sv/python-net/create-3d-mesh-and-scene/)

Här är ett exempel för att bifoga ett Phong-material till kubennoden:
### **Definiera kontrollpunkter**
En mash består av en uppsättning styrpunkter i rymden och polygoner för att beskriva maskstytan för att skapa en mask. Vi måste definiera kontrollpunkterna:

{{% alert color="primary" %}}

Kontrollpunkterna för alla geometrier i Aspose.3D använder homogen koordinat, Så det är `Vector4` istället för `Vector3` i exempelkoden.

{{% /alert %}}

**Exempel:**

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-DefineControlPoints.py" >}}


### **Skapa polygoner**
Kontrollpunkterna är inte utförbara, för att göra kuben synlig, måste vi definiera polygoner i varje sida:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-CreateMeshUsingCreatePolygons.py" >}}


### **Skapa polygoner med PolygonBuilder klass**
Vi kan också definiera polygon av hörn med `PolygonBuilder` klass:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-CreateMeshUsingPolygonBuilder.py" >}}

Nu är det klart, för att göra nätverket synligt, måste vi förbereda en nod för det.
## **Hur man kan tränga ett tåg**
Triangulera mesh är användbart för spelindustrin eftersom den trekantiga är den enda primitiva som stöds GPU-hårdvaran stöder (icke-triangulära data är triangulerad i förarnivå, som är ineffektiv i realtids rendering)

{{% alert color="primary" %}}

I denna version vi bara triangulerade polygoner eftersom det krävs av 3ds fil export, normaler/uvs och andra vertex element går förlorade under denna förfarande, vi kan genomföra detta i framtiden.

{{% /alert %}}

I detta exempel, vi triangulera en Mesh genom att importera FBX fil och sparade den i FBX format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.py" >}}
## **Skapa en 3D Cube Scene**
Detta ämne visar hur man lägger till Mesh geometri till 3D scen. Exemplet koden placerar en kub och spara 3D scen i de filformat som stöds.
### **Skapa en kubnod**
En nod är osynlig, men geometrin som är kopplad till noden kan renderas.

{{% alert color="primary" %}}

Mesh-klassobjektet används i koden. Vi kan det.[Skapa ett klassobjekt `Mesh` som berättas där.](https://docs.aspose.com/3d/python-net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Exempel**

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-CubeScene-CreateCubeScene.py" >}}

{{% alert color="primary" %}}

OBS: De enheter som är anslutna till rotnoden ignoreras vanligtvis i CAD/CAM-mjukvara, så vi behöver skapa en ny nod för att göra geometrin.

{{% /alert %}}
