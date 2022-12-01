---
title: Lägg till en tillgångsinformation och Flip koordinatsystem i 3D Format
type: docs
weight: 10
url: /sv/net/add-an-asset-information-and-flip-coordinate-system-in-3d-formats/
description: Metadata är strukturerad information som beskriver, förklarar, lokaliserar eller gör det lättare att hämta, använda eller hantera en informationsresurs. Aspose.3D for .NET API gör det möjligt för utvecklare att definiera en metadata för scenen.
---
## **Lägg till en tillgångsinformation till 3D Scene**
Metadata är strukturerad information som beskriver, förklarar, lokaliserar eller gör det lättare att hämta, använda eller hantera en informationsresurs. Aspose.3D for .NET API gör det möjligt för utvecklare att definiera en metadata för scenen.
### **Definiera en metadata för scenen**
3D visar producerar massiva mängder av metadata och bildinformation. Metadata är en tillgång och en del av showen.

1. Initiera en 3D scen med [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) klass.
1. Ange program/verktygsnamn.
1. Ange ansökan/verktygsleverantörens namn.
1. Ställ in måttenhet.
1. Ange måttenhetsskalfaktor.
1. Spara 3D scen i det stödda filformatet.

I detta exempel: Vi antar att scenen är skapad av ett CAD verktyg som kallas ”Egypten” och det är designat av ”Manualdesk”:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-AssetInformation-InformationToScene-AddAssetInformationToScene.cs" >}}
## **Flip koordinatsystem i 3D Forman**
Aspose.3D for .NET API ger användarna möjlighet att vända koordinatsystemet i OBJ. 3DS, STL och U3D format.

{{% alert color="primary" %}} 

För att importera en 3ds-fil och spara den i OBJ format [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) klassen används i koden.

{{% /alert %}} 

I detta exempel, vi vände koordinatsystem när vi importerar 3ds-filen, och sparade den i OBJ format utan material.
