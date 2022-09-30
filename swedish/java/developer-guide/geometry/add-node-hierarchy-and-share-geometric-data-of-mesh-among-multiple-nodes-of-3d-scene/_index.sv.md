---
title: Lägg Node hierarki och Dela Geometriska data av mesh bland flera noder av 3D Scene
type: docs
weight: 20
url: /sv/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java har stöd för att bygga en hierarki av noder. Noden är grundläggande byggsten av 3D scen och en hierarki av noder definierar den logiska strukturen av 0761333 481 scen. och ge synligt innehåll genom att fästa geometrier, ljus och kameror till noder.
---
## **Lägg till nodehierarki i 3D Scendokument**
Aspose.3D for Java har stöd för att bygga en hierarki av noder. `Node` är grundläggande byggsten av 3D scen och en hierarki av noder definierar den logiska strukturen i 3D scen, och ge synligt innehåll genom att fästa geometrier, ljus och kameror till noder.
### **Exempel**

I Aspose.3D kan varje `Node` instans ha flera barnnoder, i detta exempel, vi skapade en nod med två kub noder, om vi roterar rotnoden, alla barn noder påverkas också:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddNodeHierarchy.java" >}}
## **Dela meshs geometri data mellan flera noder**
För att minska minnet nödvändigheten, En enda instans av `Mesh` klass kan bindas till olika instanser av `Node` klass. Föreställ dig att du behöver ett system där alla 3D kuber verkade vara omöjligt, Men du krävde många av dem. Du kan spara minne genom att göra ett Mesh objekt när systemet börjar. Vid den punkten, varje gång du behövde en annan form, gör du ett annat Node objekt, sedan peka den noden till en `Mesh`. Detta kallas instanser. Aspose.3D for Java API tillåter att göra instanser.
### **Exempel**
I RTS (Real-time strategi) spel som, kan vi alltid se flera NPCs (Non-Player Character) med samma modell 3D, kanske i olika färger, redigeringsmotorn brukar dela samma data för maskgeometri över olika NPC, Denna teknik kallas Instancing.

{{% alert color="primary" %}} 

Klassobjektet `Mesh` används i koden. Vi kan det.[Skapa ett Mesh-klassobjekt som berättat där.](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Demonstration av exempelkod:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ShareMeshGeometryData.java" >}}


I detta exempel skapade vi 3 kub noder dela samma mesh, var och en av dem har olika material med olika färger.
