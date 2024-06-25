---
title: Lägg till nodehierarki och Dela geometriska data av mesh bland flera noder i 3D Scene
type: docs
weight: 40
url: /sv/net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for .NET erbjuder att bygga en nodehierarki. Noden är grundläggande byggsten i en scen. En hierarki av noder definierar den logiska strukturen av en scen, och ger synligt innehåll genom att fästa geometrier, ljus, och kameror till noder.
---
##  **Lägg till nodehierarki i 3D Scendokument**
Aspose.3D for .NET erbjuder att bygga en nodehierarki. Noden är grundläggande byggsten i en scen. En hierarki av noder definierar den logiska strukturen av en scen, och ger synligt innehåll genom att fästa geometrier, ljus, och kameror till noder.
###  **Exempel**
En provscen hierarki ser ut som:

![todo:image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

I Aspose. 3D, kan varje `Node` instans ha flera barnnoder, i detta exempel skapade vi en nod med två kubnoder, Om vi roterar rotnoden, alla barnnoder påverkas också:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-NodeHierarchy-AddNodeHierarchy.cs" >}}
##  **Dela meshs geometri data mellan flera noder**
För att minska minnesförnödenheter, kan en enda instans av [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) klass bindas till olika instanser av [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) klass. Föreställ dig att du behöver ett system där alla 3D kuber verkade vara oundvikliga, Men du krävde många av dem. Du kan spara minne genom att göra ett Mesh objekt när systemet börjar. Vid den punkten, varje gång du behövde en annan form, du gör en annan Node objekt, sedan peka den noden till en Mesh. Detta kallas instanser. Aspose.3D for .NET API tillåter att göra instanser.
###  **Exempel**
I RTS (Real-time strategi) spel som, kan vi alltid se flera NPCs (Non-Player Character) med samma modell 3D, kanske i olika färger, renderingsmotorn brukar dela samma data för mashgeometri med olika NPC, Denna teknik kallas Instancing.

{{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Demonstration av exempelkod:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-MeshGeometryData-ShareMeshGeometryData.cs" >}}

I detta exempel skapade vi 3 kub noder dela samma mesh, var och en av dem har olika material med olika färger.
