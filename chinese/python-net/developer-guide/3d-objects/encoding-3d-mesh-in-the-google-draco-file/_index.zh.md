---
title: 对Google Draco文件中的3D网格进行编码
type: docs
weight: 60
url: /zh/python-net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D Python via .NET API允许开发人员导入3D模型，然后在Google Draco文件中编码网格。开发人员还可以在编码网格之前指定位置，纹理坐标，颜色和正常位以及压缩级别。
---
{{% alert color="primary" %}}

[Aspose.3D为Python via .NET](https://products.aspose.com/3d/python-net/)API允许开发人员[导入3D模型](/3d/zh/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene),然后在Google Draco文件中编码网格。开发人员还可以在编码网格之前指定位置，纹理坐标，颜色和正常位以及压缩级别。

{{% /alert %}}
## **检索3D网格并在Google Draco文件中编码**
[`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)类公开的`encode`方法可用于在Google Draco文件中编码3d网格。它采用[`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh)和[`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions)对象作为参数。使用Draco保存选项，开发人员还可以在编码网格之前指定位置、纹理坐标、颜色和正常位以及压缩级别。
### **编程示例**
此代码示例检索Sphere的网格，然后在指定压缩级别后在Google Draco文件中进行编码。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.py" >}}
