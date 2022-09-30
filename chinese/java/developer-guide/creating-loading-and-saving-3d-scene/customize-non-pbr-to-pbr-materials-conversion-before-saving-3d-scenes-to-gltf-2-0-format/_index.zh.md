---
title: 在将3D场景保存到GLTF 2.0格式之前，自定义非PBR到PBR材质的转换
type: docs
weight: 50
url: /zh/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Aspose.3D for Java API的场景类表示3D场景，开发者可以通过添加各种实体来构建3D场景。
---
{{% alert color="primary" %}} 

Aspose.3D for Java API的`Scene`类表示3D场景，开发人员可以通过添加各种实体来构建3D场景。GLTF 2.0只支持PBR (基于物理的渲染) 材质，Aspose.3D API在导出为GLTF 2.0之前，将非PBR材质内部转换为PBR材质 (导出过程中场景中的材质将保持不变)，开发人员可以提供自定义转换功能来覆盖默认行为。

{{% /alert %}} 
## **非PBR到PBR材料转换**
此代码示例演示如何将材质转换为PBR材质，然后以GLTF格式保存3D场景:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Non_PBRtoPBRMaterial.java" >}}
