---
title: 3D dosya yükleme seçeneklerini C# olarak belirtin
linktitle: 3D dosya yükleme seçeneklerini belirtin
type: docs
weight: 30
url: /tr/net/specify-3d-file-load-options/
description: Tburada birkaç Scene vardır. Open yöntemi aşırı yükler veya bir Load. ptions nesnesini kabul eden aşırı yükler. Each yük formatı, bu yük formatı için yük seçeneklerini tutan ilgili bir sınıfa sahiptir.
---
##  **Overview**

This article explains how you can load different types of 3D files using their respective load option classes in C# inside the Scene object and then you can [save it in different 3D supported file formats](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). By loading and saving, you can perform number of different conversions e.g.

- Convert FBX to OBJ in C#
- Convert 3DS to FBX in C#
- Convert U3D to OBJ in C#
- Convert OBJ to 3DS in C#
- Convert X to 3DS in C#

##  **3D dosya yükleme seçenekleri**
There are several [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) method overloads or Scene class constructor overloads that accept a `LoadOptions` object. This should be an object of a class derived from the `LoadOptions` class. Each load format has a corresponding class that holds load options for that load format, for example there is `ColladaSaveOptions` for the `FileFormat.Collada` save format.
###  **Gizli 3DS yük seçeneklerinin kullanımı**
Aşağıdaki C# kodu, gizli bir 3DS dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
###  **Bj bj ptions oad ptions ptions**
Aşağıdaki C# kodu, 3D obj dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
###  **STL yük seçeneklerinin kullanımı**
Aşağıdaki C# kodu, STL dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
###  **U3D yük seçeneklerinin kullanımı**
Aşağıdaki C# kodu, U3D dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
###  **glTF yük seçeneklerinin kullanımı**
Aşağıdaki C# kodu, glTF dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.
####  **Lip lip V/T Texture ordinoordinate**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
###  **Pse of Ply Load ptions ptions**
Aşağıdaki C# kodu, PLY modelini yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
###  **DirectiX LLoad ptions ptions se**
Aşağıdaki C# kodu, directx dosyası yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
###  **Use RVM load options**
**C#**

{{< highlight "java" >}}

 // set load options of RVM

Scene scene = new Scene();

var opt = new RvmLoadOptions()

{

    CylinderRadialSegments = 32,

    DishLatitudeSegments = 16,

    DishLongitudeSegments = 24,

    TorusTubularSegments = 40

};

// import RVM

scene.Open("LAD-TOP.rvm", opt);

// save in the OBJ format

scene.Save("LAD-TOP.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
###  **Using FBX Load Options**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
