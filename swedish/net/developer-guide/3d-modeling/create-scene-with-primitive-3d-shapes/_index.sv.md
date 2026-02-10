---
title: Skapa scen med primitiv 3D Formar
type: docs
weight: 10
url: /sv/net/create-scene-with-primitive-3d-shapes/
description: Med Aspose.3D for .NET kan utvecklare definiera en scen med primitiva 3D-former. Alla parameteriserade primitive kommer att konverteras till mesh automatiskt medan spara i någon utdatafilformat som stöds.
---
{{% alert color="primary" %}}

Med [Aspose.3D for .NET](https://products.aspose.com/3d/net/) kan utvecklare definiera en scen med primitiva 3D-former. Alla parameteriserade primitive kommer att konverteras till mesh automatiskt medan spara i någon utdatafilformat som stöds.

{{% /alert %}}
##  **Bygg scen från primitiv 3D Formar**
Modellering är processen för ren skapande och Aspose.3D API stöder att skapa en scen med primitiva 3D former.
###  **Programmeringsprova**
Det här kodexemplet skapar en scen med primitiva 3D-former och sparar i filen FBX.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.RootNode.CreateChildNode("box", new Box());
// Create a Cylinder model
scene.RootNode.CreateChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
scene.Save("test.fbx");


{{< /highlight >}}
