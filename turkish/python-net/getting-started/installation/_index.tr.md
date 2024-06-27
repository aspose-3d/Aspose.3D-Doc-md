---
title: Installation
type: docs
weight: 40
url: /tr/python-net/installation/
---
##  **Sistem gereksinimleri**

First, you have to check and confirm that machine’s specifications meet the [system requirements](/3d/python-net/system-requirements/).

##  **Aspose.3D for Python via .NET kurulumu**
`pip` is the easiest way to download and install [Aspose.3D for Python via .NET](https://pypi.org/project/aspose-3d/).

To install Aspose.3D, run this command: pip install aspose-3d

##  **Using Aspose.3D for Python via .NET**

Once you finish installing the module, you can use Aspose.3D from your python code this way:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

