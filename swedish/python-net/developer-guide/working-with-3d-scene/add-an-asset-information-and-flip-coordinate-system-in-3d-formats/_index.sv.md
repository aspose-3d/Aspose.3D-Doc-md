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

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize a 3D scene
scene = Scene()
#  Set application/tool name
scene.asset_info.application_name = "Egypt"
#  Set application/tool vendor name
scene.asset_info.application_vendor = "Manualdesk"
#  We use ancient egyption measurement unit Pole
scene.asset_info.unit_name = "pole"
#  One Pole equals to 60cm
scene.asset_info.unit_scale_factor = 0.6
#  The saved file
output = "out"  + "InformationToScene.fbx"
#  Save scene to 3D supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Vänd koordinatsystem i 3D Format**
Aspose.3D for Python via .NET API tillåter användare att vända koordinatsystem i OBJ, 3DS, STL och U3D-format.

{{% alert color="primary" %}} 

För att importera en 3ds- fil och spara den i OBJ format används [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) klassen i koden.

{{% /alert %}} 

I detta exempel vände vi på koordinatsystemet när vi importerade 3ds-filen, och sparade den i OBJ format utan material.
