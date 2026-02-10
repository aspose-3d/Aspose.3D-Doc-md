---
title: Trabajar con formato VRML
type: docs
weight: 120
url: /es/python-net/working-with-vrml-format/
description: Aspose.3D for Python via .NET permite trabajar con VRML versión 1,0. El formato de archivo VRML se ha agregado a la clase FileFormat. Aspose.3D puede detectar automáticamente el formato, por lo que FileFormat generalmente se ignora en el método Open. El siguiente fragmento de código muestra el formato de archivo VRML abierto.
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,4 o superior.

{{% /alert %}} 
#  **Formato de archivo abierto VRML**
Aspose.3D for Python via .NET permite trabajar con VRML versión 1,0. Se ha agregado el formato de archivo `VRML` a la clase `FileFormat`. Aspose.3D puede detectar automáticamente el formato, por lo que el `FileFormat` generalmente se ignora en el método `open`. El siguiente fragmento de código muestra cómo abrir el formato de archivo VRML.

{{< highlight "python" >}}
from aspose.threed import Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a Scene
scene = Scene()
#  Open Virtual Reality Modeling Language (VRML) file format
scene.open("data-dir"  + "test.wrl")

{{< /highlight >}}
