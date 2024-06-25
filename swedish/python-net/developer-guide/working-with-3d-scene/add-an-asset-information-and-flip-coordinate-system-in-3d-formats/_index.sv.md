---
title: Lägg till information om tillgångar och vänd koordinatsystem i 3D Format
type: docs
weight: 10
url: /sv/python-net/add-an-asset-information-and-flip-coordinate-system-in-3d-formats/
description: Metadata är strukturerad information som beskriver, förklarar, lokaliserar eller gör det lättare att hämta, använda eller hantera en informationsresurs. Aspose.3D for Python via .NET API tillåter utvecklare att definiera en metadata för scenen.
---
##  **Lägg till en information om tillgångar till 3D Scene**
Metadata är strukturerad information som beskriver, förklarar, lokaliserar eller gör det lättare att hämta, använda eller hantera en informationsresurs. Aspose.3D for Python via .NET API tillåter utvecklare att definiera en metadata för scenen.
###  **Definiera en metadata för scenen**
3D visar tillverkar stora mängder av metadata och bildinformation. Metadata är en tillgång och en del av showen.

1. Initiera en 3D scen med `Scene` klass.
1. Ange program/verktygsnamn.
1. Ange ansökan/verktygsleverantörens namn.
1. Ställ in måttenhet.
1. Ange måttenhetsskalfaktor.
1. Spara 3D-scenen i det stödda filformatet.

I det här exemplet antar vi att scenen är skapad av ett CAD-verktyg som heter “Egypt” och det är designat av “Manualdesk”:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "AssetInformation-InformationToScene-AddAssetInformationToScene.py" >}}
##  **Vänd koordinatsystem i 3D Format**
Aspose.3D for Python via .NET API tillåter användare att vända koordinatsystem i OBJ, 3DS, STL och U3D-format.

{{% alert color="primary" %}} 

För att importera en 3ds- fil och spara den i OBJ format används [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) klassen i koden.

{{% /alert %}} 

I detta exempel vände vi på koordinatsystemet när vi importerade 3ds-filen, och sparade den i OBJ format utan material.
