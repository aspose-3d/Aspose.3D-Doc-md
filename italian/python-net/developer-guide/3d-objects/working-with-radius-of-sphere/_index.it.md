---
title: Lavorare con il raggio della sfera
type: docs
weight: 110
url: /it/python-net/working-with-radius-of-sphere/
description: Utilizzando Aspose.3D for Python via .NET, è possibile impostare il raggio di ottenere di una sfera. Per ottenere o impostare il raggio, è possibile utilizzare la proprietà Raggio della classe Sphere. Di seguito è riportato il codice di esempio per impostare il raggio di una sfera.
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.4 o maggiore.

{{% /alert %}} 
##  **Lavoro con il raggio della sfera**
Utilizzando Aspose.3D for Python via .NET, è possibile impostare il raggio di ottenere di una sfera. Per ottenere o impostare il raggio, puoi utilizzare la proprietà `radius` della classe `Sphere`. Di seguito è riportato il codice di esempio per impostare il raggio di una sfera.

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a Scene
scene = Scene()
sphere = Sphere()
sphere.radius = 10 .0
#  Set Sphere Radius (Using Radius property you can get or set radius of Sphere)
scene.root_node.create_child_node(sphere)
#  Save scene
scene.save("data-dir"  + "sphere.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
