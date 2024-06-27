---
title: Преобразование Mesh одного объекта 3D в файл PLY
type: docs
weight: 20
url: /ru/net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Для преобразования сетки объекта 3D в файл PLY можно использовать перегруженные члены EncodeMesh, выставленные классом PlyFormat. Члены EncodeMesh принимают в качестве параметров Mesh, имя выходного файла и объекты PlySaveOptions. Используя параметры сохранения PLY, разработчики могут изменить имя компонентов координат.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API позволяет разработчикам конвертировать сетку одного объекта 3D в файл PLY.

{{% /alert %}}
##  **Создайте объект 3D и сохраните его в файле PLY**
Перезагруженные участники `EncodeMesh`, выставленные классом `PlyFormat`, могут быть использованы для преобразования `Mesh` объекта 3D в файл PLY. Участники `EncodeMesh` принимают `Mesh`, имя выходного файла и объекты `PlySaveOptions` в качестве параметров. Используя параметры сохранения PLY, разработчики могут изменить имя компонентов координат.
###  **Образец программирования**
Этот пример кода создает объект 3D Cylinder, а затем кодируют в файле PLY.

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
