---
title: 3D sahnelerini GLTF 2.0 formatında C# 'dan tasarruf etmeden önce pbr olmayan malzemeleri dönüştürmeye özelleştirin
linktitle: Customize Non-PBR to PBR Materials Conversion before Saving 3D Scenes to GLTF 2.0 Format
type: docs
weight: 70
url: /tr/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: The Scene class of the Aspose.3D API represents a 3D scene. Developers can already build a 3D scene by adding various entities. GLTF 2.0 only supports PBR (Physically Based Rendering) materials, Aspose.3D API internally converts non-PBR materials into PBR materials before exporting into GLTF 2.0.
---
{{% alert color="primary" %}} 

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class of the Aspose.3D API represents a 3D scene. Developers can already build a 3D scene by adding various entities. GLTF 2.0 only supports PBR (Physically Based Rendering) materials, Aspose.3D API internally converts non-PBR materials into PBR materials before exporting into GLTF 2.0 (the materials in the scene will remain unchanged during the export), and the developers can provide custom convert function to override the default behavior.

{{% /alert %}} 
##  **Non-PBto to PBerial erial aterial erial onversion**
Bu C# kod örneği, malzemeyi pbr malzemesine nasıl dönüştüreceğinizi gösterir ve daha sonra 3D görüntüsünü GLTF formatında C# 3D dosya manipülasyonu ve dönüştürme API ile kaydeder:

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


##  **Resources**

1. [Çevrimiçi öğretici](https://products.aspose.com/3d/tutorial/use-phong-material-to-pbr-material/)
