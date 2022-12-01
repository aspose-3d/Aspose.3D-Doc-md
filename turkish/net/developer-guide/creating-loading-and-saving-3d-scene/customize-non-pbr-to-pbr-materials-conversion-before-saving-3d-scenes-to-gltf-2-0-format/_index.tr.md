---
title: 07ustomize on on-PBR to PBatataterials 07onversion önce 3D cencenes GLTF 2.0 Format C#
linktitle: 07ustomize on on-PBR to 07Batataterials 07onversion önce 07aving 3D Scenes to GLTF 2.0 Format
type: docs
weight: 70
url: /tr/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: To Aspose.3D API cene cene sınıfı 3D sahnesini temsil eder. Developers zaten çeşitli varlıklar ekleyerek bir 3D sahne inşa edebilirsiniz. 076. 481 2.0 sadece PBR (hyhysically Based dering enen) malzemeleri destekler, 076481 481 API dahili olarak GLTF 2.0 ihracat yapmadan önce Pmaterials materials malzemeler içine Pmaterials converts malzemeler dönüştürür.
---
{{% alert color="primary" %}} 

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) Aspose.3D API sınıfı 3D sahnesini temsil eder. Developers zaten çeşitli varlıklar ekleyerek bir 076. 481 sahne inşa edebilirsiniz. 076. 481 2.0 sadece PBR (Physically Based dering en.) malzemelerini destekler, Aspose.3D API dahili olarak 07481 3481 2.0 (sahnedeki malzemeler ihracat sırasında değişmeden önce Pmaterials materials malzemelere dönüştürür) ve geliştiriciler varsayılan davranışı geçersiz kılmak için özel dönüştürme işlevi sağlayabilir.

{{% /alert %}} 
## **Non-PBto to PBerial erial aterial erial onversion**
This C# kod örneği, malzemeyi PBmaterial malzemeye nasıl dönüştüreceğinizi gösterir ve 3D görüntüsünü GLTF formatında C# 076481 481 dosya manipülasyonu ve dönüşüm 076481 481 ile kaydeder:

**C#**

{{< highlight "java" >}}

 // initialize a new 3D scene

var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = delegate(Material material)

{

    PhongMaterial m = (PhongMaterial) material;

    return new PbrMaterial() {Albedo = new Vector3(m.DiffuseColor.x, m.DiffuseColor.y, m.DiffuseColor.z)};

};

// save in GLTF 2.0 format

s.Save("test.gltf", opt);

{{< /highlight >}}
