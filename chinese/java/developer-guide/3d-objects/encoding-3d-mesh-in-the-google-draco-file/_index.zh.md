---
title: 编码 Google Draco 文件中的 3D 网格
type: docs
weight: 30
url: /zh/java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Java API 支持在 Google Draco 文件中导入 3D 模型、检索网格，然后对网格进行编码。
---
{{% alert color="primary" %}} 

Aspose.3D for Java API 支持在 Google Draco 文件中导入 3D 模型、检索网格，然后对网格进行编码。开发人员还可以在编码网格之前指定位置，纹理坐标，颜色和正常位以及压缩级别。

{{% /alert %}} 
##  **在 Google Draco 文件中检索 3D 网格和编码**
`DracoFormat` 类公开的encode方法可用于对 Google Draco 文件中的 3D 网格进行编码。它采用 `Mesh` 和 `DracoSaveOptions` 对象作为参数。使用 Draco 保存选项，开发人员还可以在编码网格之前指定位置，纹理坐标，颜色和正常位以及压缩级别。
###  **编程示例**
此代码示例检索球体的网格，然后在指定压缩级别后在 Google Draco 文件中进行编码。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-Encode3DMeshinGoogleDraco.java" >}}
