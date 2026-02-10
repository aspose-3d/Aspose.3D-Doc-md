---
title: Szene mit primitiven 3D Formen erstellen
type: docs
weight: 20
url: /de/java/create-scene-with-primitive-3d-shapes/
description: Aspose.3D for Java API unterstützt primitive 3D Formen. Alle param etrisierten Grundelemente werden automatisch in Mesh konvertiert, während in einem beliebigen unterstützten Ausgabe dateiformat gespeichert wird.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API unterstützt primitive 3D Formen. Alle param etrisierten Grundelemente werden automatisch in Mesh konvertiert, während in einem beliebigen unterstützten Ausgabe dateiformat gespeichert wird.

{{% /alert %}} 
##  **Erstellen Sie eine Szene aus primitiven 3D Formen**
Modellierung ist der Prozess der reinen Schöpfung und Aspose.3D API unterstützt das Erstellen einer Szene mit primitiven 3D Formen.
###  **Programmier probe**
In diesem Code beispiel wird eine Szene mit primitiven 3D-Formen erstellt und in der FBX-Datei gespeichert.

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
