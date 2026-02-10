---
title: Szene mit primitiven 3D Formen erstellen
type: docs
weight: 10
url: /de/python-net/create-scene-with-primitive-3d-shapes/
description: Mit Aspose.3D for Python via .NET können Entwickler eine Szene mit primitiven 3D Formen definieren. Alle param etrisierten Grundelemente werden automatisch in Mesh konvertiert, während in einem beliebigen unterstützten Ausgabe dateiformat gespeichert wird.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) können Entwickler eine Szene mit primitiven 3D Formen definieren. Alle param etrisierten Grundelemente werden automatisch in Mesh konvertiert, während in einem beliebigen unterstützten Ausgabe dateiformat gespeichert wird.

{{% /alert %}}
##  **Erstellen Sie eine Szene aus primitiven 3D Formen**
Modellierung ist der Prozess der reinen Schöpfung und Aspose.3D API unterstützt das Erstellen einer Szene mit primitiven 3D Formen.
###  **Programmier probe**
In diesem Code beispiel wird eine Szene mit primitiven 3D-Formen erstellt und in der FBX-Datei gespeichert.

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
