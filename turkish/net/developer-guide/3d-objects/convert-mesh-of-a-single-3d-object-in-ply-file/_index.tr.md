---
title: Tek bir 3D nesnesinin ağını PLY dosyasında dönüştürün
type: docs
weight: 20
url: /tr/net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Plyformat sınıfı tarafından maruz kalan aşırı yüklü encodemesh üyeleri, 3D nesnesinin ağını PLY dosyasına dönüştürmek için kullanılabilir. Encodemesh üyeleri örgü, çıkış dosya adı ve plysaveoptions nesnelerini parametreler olarak alır. PLY kaydetme seçeneklerini kullanarak, geliştiriciler koordinat bileşenlerinin adını değiştirebilir.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API allows developers to convert the Mesh of a single 3D object in the PLY file.

{{% /alert %}}
##  **3D nesnesi oluşturun ve PLY dosyasına kaydedin**
The overloaded `EncodeMesh` members exposed by the `PlyFormat` class can be used to convert the `Mesh` of a 3D object to PLY file. The `EncodeMesh` members take the `Mesh`, output file name and `PlySaveOptions` objects as parameters. Using the PLY save options, developers can change the name of coordinate components.
###  **Programming ample ample**
Bu kod örneği bir 3D silindir nesnesi oluşturur ve daha sonra PLY dosyasında kodlanır.

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
