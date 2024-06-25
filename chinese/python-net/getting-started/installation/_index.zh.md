---
title: Installation
type: docs
weight: 40
url: /zh/python-net/installation/
---
##  **系统要求**

首先，您必须检查并确认机器的规格符合 [系统要求](/3d/zh/python-net/system-requirements/)。

##  **正在安装 Aspose.3D for Python via .NET**
`pip` 是下载和安装 [Aspose.3D for Python via .NET](https://pypi.org/project/aspose-3d/) 的最简单方法。

若要安装 Aspose.3D，请运行以下命令: pip install aspose-3d

##  **正在使用 Aspose.3D for Python via .NET**

一旦你完成安装模块，你可以使用 Aspose。3D 从你的python代码这样:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

