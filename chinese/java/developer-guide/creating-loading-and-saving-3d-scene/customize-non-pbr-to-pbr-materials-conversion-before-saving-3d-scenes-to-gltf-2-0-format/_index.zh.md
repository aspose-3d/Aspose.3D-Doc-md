---
title: 在将 3D 个场景保存为 GLTF 个2.0格式之前，自定义非PBR到PBR材质的转换
type: docs
weight: 50
url: /zh/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Aspose.3D for Java API 的场景类表示 3D 场景，开发人员可以通过添加各种实体来构建 3D 场景。
---
{{% alert color="primary" %}} 

Aspose.3D for Java API 的 `Scene` 类表示 3D 场景，开发人员可以通过添加各种实体来构建 3D 场景。GLTF 2.0仅支持PBR (基于物理的渲染) 材质，Aspose.3D API 将非PBR材质内部转换为PBR材质，然后导出为 GLTF 2.0 (导出时场景中的材质将保持不变)，并且开发人员可以提供自定义转换函数来覆盖默认行为。

{{% /alert %}} 
##  **非PBR到PBR材料转换**
此代码示例演示如何将材质转换为PBR材质，然后以 GLTF 格式保存 3D 场景:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Non_PBRtoPBRMaterial.java" >}}
