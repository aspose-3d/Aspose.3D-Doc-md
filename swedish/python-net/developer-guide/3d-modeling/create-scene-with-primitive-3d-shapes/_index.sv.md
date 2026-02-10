---
title: Skapa scen med primitiv 3D Formar
type: docs
weight: 10
url: /sv/python-net/create-scene-with-primitive-3d-shapes/
description: Med Aspose.3D for Python via .NET kan utvecklare definiera en scen med primitiva 3D-former. Alla parameteriserade primitive kommer att konverteras till mesh automatiskt medan spara i någon utdatafilformat som stöds.
---
{{% alert color="primary" %}}

Med [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) kan utvecklare definiera en scen med primitiva 3D-former. Alla parameteriserade primitive kommer att konverteras till mesh automatiskt medan spara i någon utdatafilformat som stöds.

{{% /alert %}}
##  **Bygg scen från primitiv 3D Formar**
Modellering är processen för ren skapande och Aspose.3D API stöder att skapa en scen med primitiva 3D former.
###  **Programmeringsprova**
Det här kodexemplet skapar en scen med primitiva 3D-former och sparar i filen FBX.

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Box, Cylinder

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
#  Initialize a Scene object
scene = Scene()
#  Create a Box model
scene.root_node.create_child_node("box", Box())
#  Create a Cylinder model
scene.root_node.create_child_node("cylinder", Cylinder())
#  Save drawing in the FBX format
output = "out"  + "test.fbx"
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
