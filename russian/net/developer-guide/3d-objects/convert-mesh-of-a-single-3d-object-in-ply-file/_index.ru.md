---
title: Преобразование сетки одного объекта 3D в файле PLY
type: docs
weight: 20
url: /ru/net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Перегруженные члены EncodeMesh, открытые классом PlyFormat, могут использоваться для преобразования сетки объекта 3D в файл PLY. Члены EncodeMesh принимают в качестве параметров объекты Mesh, имя выходного файла и PlySaveOptions. Используя параметры сохранения PLY, разработчики могут изменить имя компонентов координат.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API позволяет разработчикам преобразовывать Mesh одного объекта 3D в файл PLY.

{{% /alert %}}
## **Создайте объект 3D и сохраните его в файл PLY**
Перегруженные члены `EncodeMesh`, открытые классом `PlyFormat`, могут использоваться для преобразования `Mesh` объекта 3D в файл PLY. Члены `EncodeMesh` принимают в качестве параметров `Mesh`, имя выходного файла и объекты `PlySaveOptions`. Используя параметры сохранения PLY, разработчики могут изменить имя компонентов координат.
### **Образец программирования**
Этот пример кода создает объект 3D Cylinder, а затем кодирует в файле PLY.

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
