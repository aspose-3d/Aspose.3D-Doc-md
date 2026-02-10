---
title: Szene mit primitiven 3D Formen erstellen
type: docs
weight: 10
url: /de/net/create-scene-with-primitive-3d-shapes/
description: Mit Aspose.3D for .NET können Entwickler eine Szene mit primitiven 3D Formen definieren. Alle param etrisierten Grundelemente werden automatisch in Mesh konvertiert, während in einem beliebigen unterstützten Ausgabe dateiformat gespeichert wird.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for .NET](https://products.aspose.com/3d/net/) können Entwickler eine Szene mit primitiven 3D Formen definieren. Alle param etrisierten Grundelemente werden automatisch in Mesh konvertiert, während in einem beliebigen unterstützten Ausgabe dateiformat gespeichert wird.

{{% /alert %}}
##  **Erstellen Sie eine Szene aus primitiven 3D Formen**
Modellierung ist der Prozess der reinen Schöpfung und Aspose.3D API unterstützt das Erstellen einer Szene mit primitiven 3D Formen.
###  **Programmier probe**
In diesem Code beispiel wird eine Szene mit primitiven 3D-Formen erstellt und in der FBX-Datei gespeichert.

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
