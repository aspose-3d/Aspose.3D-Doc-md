---
title: Кодирование сетки 3D в файле Google Draco
type: docs
weight: 60
url: /ru/python-net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D для Python via .NET API позволяет разработчикам импортировать модель 3D, а затем кодировать сетки в файлах Google Draco. Разработчики также могут указать положение, координаты текстуры, цвет и нормальные биты, а также уровень сжатия перед кодированием сетки.
---
{{% alert color="primary" %}}

[Aspose.3D для Python via .NET](https://products.aspose.com/3d/python-net/)API позволяет разработчикам[Импортировать модель 3D](/3d/ru/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), А затем кодировать сетки в файлах Google Draco. Разработчики также могут указать положение, координаты текстуры, цвет и нормальные биты, а также уровень сжатия перед кодированием сетки.

{{% /alert %}}
## **Извлечь сетку 3D и закодировать в файле Google Draco**
Метод `encode`, представленный классом [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat), можно использовать для кодирования трехмерной сетки в файле Google Draco. В качестве параметров он принимает объекты [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) и [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions). Используя параметры сохранения Draco, разработчики также могут указать положение, координаты текстуры, цвет и обычные биты, а также уровень сжатия перед кодированием сетки.
### **Образец программирования**
Этот пример кода извлекает Сетка Сферы, а затем кодирует в файле Google Draco после указания уровня сжатия.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.py" >}}
