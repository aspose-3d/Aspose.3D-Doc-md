---
title: 安装
type: docs
weight: 40
url: /zh/python-net/installation/
---
## **系统要求**

首先，您必须检查并确认机器的规格是否符合[系统要求](/3d/zh/python-net/system-requirements/)。

## **为Python via .NET安装Aspose.3D**
`pip`是下载和安装最简单的方法[Aspose.3D为Python via .NET](https://pypi.org/project/aspose-3d/)。

要安装Aspose.3D，请运行以下命令: pip安装aspose-3d

## **使用Aspose.3D进行Python via .NET**

完成安装模块后，您可以通过以下方式使用python代码中的Aspose.3D:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

