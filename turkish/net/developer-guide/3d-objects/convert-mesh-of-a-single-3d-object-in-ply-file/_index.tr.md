---
title: PLY dosyasında tek bir 3D nesnesinin vert onvert Mesh
type: docs
weight: 20
url: /tr/net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Po aşırı yüklü Encode. esh üyeleri Plylyormat sınıfı tarafından maruz bırakılan bir 3D nesnesinin Mesh PLY dosyasına dönüştürmek için kullanılabilir. The Encode. esh üyeleri Mesh, çıktı dosya adı ve Ply. ave. objects nesnelerini parametreler olarak alır. PLY kaydetme seçeneklerini kaydetme, geliştiriciler koordinat bileşenlerinin adını değiştirebilir.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API, geliştiricilerin PLY dosyasında tek bir 3D nesnesinin değerini dönüştürmelerine izin verir.

{{% /alert %}}
## **C3D nesnesini yeniden hazırlayın ve PLY dosyasına kaydedin**
`PlyFormat` sınıfı tarafından maruz kalan `EncodeMesh` üyelerini aşırı yükledi, 3D nesnesinin 076481 481 dosyasına `Mesh` 'ü dönüştürmek için kullanılabilir. The 076. 481 üyeleri `Mesh`, çıkış dosyası adı ve `PlySaveOptions` nesnelerini parametreler olarak alır. 07. 3481 kaydetme seçeneklerini kaydetme, geliştiriciler koordinat bileşenlerinin adını değiştirebilir.
### **Programming ample ample**
Tkod örneği 3D Cylinder nesnesini oluşturur ve sonra PLY dosyasında kodlanır.

**C#**

{{< highlight "java" >}}

 // Create a cylinder object and save it to ply file

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply");

/* using Ply save options*/

//Save as binary PLY format, the default value is ASCII

PlySaveOptions opt = new PlySaveOptions(FileContentType.Binary);

//change the components to 's' and 't'

opt.TextureCoordinateComponents.Item1 = "s";

opt.TextureCoordinateComponents.Item2 = "t";

//save the mesh

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply", opt);

{{< /highlight >}}
