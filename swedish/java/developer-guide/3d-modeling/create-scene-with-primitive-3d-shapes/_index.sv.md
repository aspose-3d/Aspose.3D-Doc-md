---
title: Skapa scen med primitiv 3D Formar
type: docs
weight: 20
url: /sv/java/create-scene-with-primitive-3d-shapes/
description: Aspose.3D for Java API har stöd för primitiva 3D former. Alla parameteriserade primitive kommer att konverteras till mesh automatiskt medan spara i någon utdatafilformat som stöds.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API har stöd för primitiva 3D former. Alla parameteriserade primitive kommer att konverteras till mesh automatiskt medan spara i någon utdatafilformat som stöds.

{{% /alert %}} 
##  **Bygg scen från primitiv 3D Formar**
Modellering är processen för ren skapande och Aspose.3D API stöder att skapa en scen med primitiva 3D former.
###  **Programmeringsprova**
Det här kodexemplet skapar en scen med primitiva 3D-former och sparar i filen FBX.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.getRootNode().createChildNode("box", new Box());
// Create a Cylinder model
scene.getRootNode().createChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
MyDir = MyDir + RunExamples.getOutputFilePath("test.fbx");
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
