---
title: Specify 3D File Load ptions ptions in C#
linktitle: Specify 3D File ptions oad ptions ptions
type: docs
weight: 30
url: /tr/net/specify-3d-file-load-options/
description: Tburada birkaç Scene vardır. Open yöntemi aşırı yükler veya bir Load. ptions nesnesini kabul eden aşırı yükler. Each yük formatı, bu yük formatı için yük seçeneklerini tutan ilgili bir sınıfa sahiptir.
---
## **Overview**

Tonun makalesi, ilgili yük seçeneği sınıflarını C# 'de Scene nesnesinin içine kullanarak 3D dosyalarının farklı türlerini nasıl yükleyebileceğinizi açıklıyor ve sonra yapabilirsiniz[Farklı 3D desteklenen dosya formatlarında kaydedin](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). By yükleme ve kaydetme, örneğin farklı dönüşüm sayısını gerçekleştirebilirsiniz

- Convert FBX OBJ C#
- Convert 3DS FBX C#
- Convert U3D OBJ C#
- Convert OBJ 3DS C#
- C# yılında 07onvert X to 3DS

## **3D File Load ptions ptions**
Tburada [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) yöntemi aşırı yükler veya `LoadOptions` nesnesini kabul eden Scene sınıfı oluşturucu aşırı yükler vardır. This `LoadOptions` sınıfından türetilen bir sınıfın nesnesi olmalıdır. Each yük formatı, bu yük formatı için yük seçeneklerini tutan ilgili bir sınıfa sahiptir, örneğin 076. 481 kaydetme formatı için `ColladaSaveOptions` vardır.
### **Discreet 3DS Load ptions ptions ptions**
The C# kodu aşağıda, bir 07iscreet 3DS dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
### **Bj bj ptions oad ptions ptions**
The C# kod aşağıda bir 3D Obj dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
### **Use of STL ptions oad ptions ptions**
The C# kodu aşağıda, STL dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
### **Use of U3D ptions oad ptions ptions**
The C# kodu aşağıda, U3D dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
### **Use of glTF ptions oad ptions ptions**
The C# kodu aşağıda, glTF dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.
#### **Lip lip V/T Texture ordinoordinate**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
### **Pse of Ply Load ptions ptions**
The C# kodu aşağıda, PLY modelini yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
### **Use of DirectX X Load ptions ptions**
The C# kod aşağıda, DirectX X dosyasını yüklemeden önce yük seçeneklerinin nasıl ayarlanacağını gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
### **Use RVM yük seçenekleri**
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
### **Using FBX Load ptions ptions**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
