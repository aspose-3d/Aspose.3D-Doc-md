---
title: 在将 3D 场景保存为 C# 中的 GLTF 2.0格式之前，自定义非PBR到PBR材质转换
linktitle: 在将 3D 个场景保存为 GLTF 个2.0格式之前，自定义非PBR到PBR材质的转换
type: docs
weight: 70
url: /zh/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Aspose 的场景类。3D API 表示 3D 场景。开发人员已经可以通过添加各种实体来构建 3D 场景。GLTF 2.0仅支持PBR (基于物理的渲染) 材质，Aspose。3D API 将非PBR材质内部转换为PBR材质，然后导出为 GLTF 2.0。
---
{{% alert color="primary" %}} 

Aspose.3D API 的 [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) 类表示 3D 场景。开发人员已经可以通过添加各种实体来构建 3D 场景。GLTF 2.0仅支持PBR (物理渲染) 材质，Aspose.3D API 将非PBR材质内部转换为PBR材质，然后导出为 GLTF 2.0 (导出时场景中的材质将保持不变)，并且开发人员可以提供自定义转换函数来覆盖默认行为。

{{% /alert %}} 
##  **非PBR到PBR材料转换**
此 C# 代码示例演示如何将材质转换为PBR材质，然后使用 C# 3D 文件操作和转换 API 以 GLTF 格式保存 3D 场景:

**C#**

{{< highlight "java" >}}

 // initialize a new 3D scene

var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = (Material material) => {
    var pbr = PbrMaterial.FromMaterial(material);
    //customize your own PBR material here, you can get the original OBJ's material from the parameter mat.
    //to create a compatible material with obj2gltf, use following definition:
    pbr.MetallicFactor = 0;
    pbr.RoughnessFactor = 0.98;
    return pbr;
};

// save in GLTF 2.0 format

s.Save("test.gltf", opt);

{{< /highlight >}}


##  **资源**

1. [在线教程](https://products.aspose.com/3d/tutorial/use-phong-material-to-pbr-material/)
