---
title: Lägg Node hierarki och Dela Geometriska data av mesh bland flera noder av 3D Scene
type: docs
weight: 40
url: /sv/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D för Python via .NET erbjuder att bygga en Node hierarki. Noden är grundläggande byggsten i en scen. En hierarki av noder definierar den logiska strukturen av en scen, och ger synligt innehåll genom att fästa geometrier, ljus, och kameror till noder.
---
## **Lägg till nodehierarki i 3D Scendokument**
Aspose.3D för Python via .NET erbjuder att bygga en Node hierarki. Noden är grundläggande byggsten i en scen. En hierarki av noder definierar den logiska strukturen av en scen, och ger synligt innehåll genom att fästa geometrier, ljus, och kameror till noder.
### **Exempel**
En provscen hierarki ser ut som:

![TOD:imageName_Av_Text:](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

I Aspose.3D kan varje `Node` instans ha flera barnnoder, i detta exempel, vi skapade en nod med två kub noder, om vi roterar rotnoden, alla barn noder påverkas också:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-NodeHierarchy-AddNodeHierarchy.py" >}}
## **Dela meshs geometri data mellan flera noder**
För att minska minnet nödvändigheten, En enda instans av [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) klass kan bindas till olika instanser av [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) klass. Föreställ dig att du behöver ett system där alla 3D kuber verkade vara omöjligt, Men du krävde många av dem. Du kan spara minne genom att göra ett Mesh objekt när systemet börjar. Vid den punkten, varje gång du behövde en annan form, du gör en annan Node objekt, sedan peka den noden till en Mesh. Detta kallas instanser. Aspose.3D för Python via .NET API tillåter att göra instanser.
### **Exempel**
I RTS (Real-time strategi) spel som, kan vi alltid se flera NPCs (Non-Player Character) med samma modell 3D, kanske i olika färger, redigeringsmotorn brukar dela samma data för maskgeometri över olika NPC, Denna teknik kallas Instancing.

{{% alert color="primary" %}}

Klassobjektet `Mesh` används i koden. Vi kan det.[Skapa ett klassobjekt `Mesh` som berättas där.](/3d/sv/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Demonstration av exempelkod:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MeshGeometryData-ShareMeshGeometryData.py" >}}

I detta exempel skapade vi 3 kub noder dela samma mesh, var och en av dem har olika material med olika färger.
