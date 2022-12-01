---
title: 转换PLY文件中单个3D对象的网格
type: docs
weight: 20
url: /zh/net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: PlyFormat类公开的重载EncodeMesh成员可用于将3D对象的网格转换为PLY文件。EncodeMesh成员将网格，输出文件名和PlySaveOptions对象作为参数。使用PLY保存选项，开发人员可以更改坐标组件的名称。
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API允许开发人员转换PLY文件中单个3D对象的网格。

{{% /alert %}}
## **创建3D对象并将其保存到PLY文件**
`PlyFormat`类公开的重载`EncodeMesh`成员可用于将3D对象的`Mesh`转换为PLY文件。`EncodeMesh`成员将`Mesh`、输出文件名和`PlySaveOptions`对象作为参数。使用PLY保存选项，开发人员可以更改坐标组件的名称。
### **编程示例**
此代码示例创建一个3D圆柱体对象，然后在PLY文件中进行编码。

**C#**

{{< highlight "java" >}}

 // Create a cylinder object and save it to ply file

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply");

/* using Ply save options*/

//Save as binary PLY format, the default value is ASCII

PlySaveOptions opt = new PlySaveOptions(FileContentType.Binary);

//change the components to 's' and 't'

opt.TextureCoordinateComponents.Item1 = "s";

opt.TextureCoordinateComponents.Item2 = "t";

//save the mesh

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply", opt);

{{< /highlight >}}
