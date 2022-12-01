---
title: 对Google Draco文件中的3D网格进行编码
type: docs
weight: 30
url: /zh/java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Java API支持导入3D模型，检索网格，然后在Google Draco文件中编码网格。
---
{{% alert color="primary" %}} 

Aspose.3D for Java API支持导入3D模型，检索网格，然后在Google Draco文件中编码网格。开发人员还可以在编码网格之前指定位置，纹理坐标，颜色和正常位以及压缩级别。

{{% /alert %}} 
## **检索3D网格并在Google Draco文件中编码**
`DracoFormat`类公开的encode方法可用于对Google Draco文件中的3D网格进行编码。它采用`Mesh`和`DracoSaveOptions`对象作为参数。使用Draco保存选项，开发人员还可以在编码网格之前指定位置，纹理坐标，颜色和正常位以及压缩级别。
### **编程示例**
此代码示例检索Sphere的网格，然后在指定压缩级别后在Google Draco文件中进行编码。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-Encode3DMeshinGoogleDraco.java" >}}
