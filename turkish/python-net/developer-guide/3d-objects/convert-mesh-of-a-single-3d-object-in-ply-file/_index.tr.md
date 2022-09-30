---
title: PLY dosyasında tek bir 3D nesnesinin vert onvert Mesh
type: docs
weight: 20
url: /tr/python-net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Po aşırı yüklü Encode. esh üyeleri Plylyormat sınıfı tarafından maruz bırakılan bir 3D nesnesinin Mesh PLY dosyasına dönüştürmek için kullanılabilir. The Encode. esh üyeleri Mesh, çıktı dosya adı ve Ply. ave. objects nesnelerini parametreler olarak alır. PLY kaydetme seçeneklerini kaydetme, geliştiriciler koordinat bileşenlerinin adını değiştirebilir.
---
{{% alert color="primary" %}}

[Python via .NET için Aspose.3D](https://products.aspose.com/3d/python-net/)API, geliştiricilerin PLY dosyasında tek bir 3D nesnesinin değerini dönüştürmelerine izin verir.

{{% /alert %}}
## **C3D nesnesini yeniden hazırlayın ve PLY dosyasına kaydedin**
`PlyFormat` sınıfı tarafından maruz kalan `encodeMesh` üyelerini aşırı yükledi, 3D nesnesinin Mesh dosyasını PLY dosyasına dönüştürmek için kullanılabilir. The 076. 481 üyeleri 076. 481, çıkış dosyası adı ve `PlySaveOptions` nesnelerini parametreler olarak alır. PLY kaydetme seçeneklerini kaydetme, geliştiriciler koordinat bileşenlerinin adını değiştirebilir.
### **Programming ample ample**
Tkod örneği 3D Cylinder nesnesini oluşturur ve sonra PLY dosyasında kodlanır.

**Python**

```py

from aspose.threed import FileFormat, FileContentType
from aspose.threed.entities import Cylinder
from aspose.threed.formats import PlySaveOptions

# Create a cylinder object and save it to ply file

FileFormat.PLY.encode_mesh(Cylinder(), "cylinder.ply")

# using Ply save options

# Save as binary PLY format, the default value is ASCII

opt = PlySaveOptions(FileContentType.BINARY)

# change the components to 's' and 't'

opt.texture_coordinate_components.item1 = "s
opt.texture_coordinate_components.item2 = "t"

# save the mesh

FileFormat.PLY.encode_mesh(Cylinder(), "cylinder.ply", opt)

```
