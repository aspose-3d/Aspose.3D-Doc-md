---
title: VRML formatı ile çalışmak
type: docs
weight: 120
url: /tr/python-net/working-with-vrml-format/
description: Aspose.3D for Python via .NET allows working with VRML version 1.0. VRML file format has been added to the FileFormat class. Aspose.3D can auto detect the format, so the FileFormat is usually ignored in Open method. The following code snippet shows how open VRML file format.
---
{{% alert color="primary" %}} 

This özelliği 19.4 veya daha büyük sürümle desteklenir.

{{% /alert %}} 
#  **Open VRML File Format**
Aspose.3D for Python via .NET allows working with VRML version 1.0. `VRML` file format has been added to the `FileFormat` class. Aspose.3D can auto detect the format, so the `FileFormat` is usually ignored in `open` method. The following code snippet shows how open VRML file format.

{{< highlight "python" >}}
from aspose.threed import Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a Scene
scene = Scene()
#  Open Virtual Reality Modeling Language (VRML) file format
scene.open("data-dir"  + "test.wrl")

{{< /highlight >}}
