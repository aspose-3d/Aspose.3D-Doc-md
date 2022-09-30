---
title: 在将3D场景保存到GLTF 2.0格式之前，自定义非PBR到PBR材质的转换
type: docs
weight: 70
url: /zh/python-net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Aspose.3D API的场景类表示3D场景。开发人员已经可以通过添加各种实体来构建3D场景。GLTF 2.0仅支持PBR (基于物理的渲染) 材料，Aspose.3D API在内部将非PBR材料转换为PBR材料，然后再导出为GLTF 2.0。
---
{{% alert color="primary" %}} 

Aspose.3D API的[`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)类表示3D场景。开发人员已经可以通过添加各种实体来构建3D场景。GLTF 2.0只支持PBR (基于物理的渲染) 材质，Aspose.3D API在导出为GLTF 2.0之前，将非PBR材质内部转换为PBR材质 (导出过程中场景中的材质将保持不变)，开发人员可以提供自定义转换功能来覆盖默认行为。

{{% /alert %}} 
## **非PBR到PBR材料转换**
此代码示例演示如何将材质转换为PBR材质，然后以GLTF格式保存3D场景:

**C#**

```py

import aspose.threed as a3d

# initialize a new 3D scene

s = a3d.Scene()

box = a3d.Box()

mat = a3d.shading.PhongMaterial()
mat.diffuse_color = Vector3(1, 0, 1)

s.root_node.create_child_node("box1", box).material = mat

opt = a3d.formats.GLTFSaveOptions(FileFormat.GLTF2);

# save in GLTF 2.0 format

s.save("test.gltf", opt);

```
