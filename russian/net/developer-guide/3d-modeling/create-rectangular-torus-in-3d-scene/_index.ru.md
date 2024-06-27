---
title: Создайте прямоугольного тора в сцене 3D
type: docs
weight: 50
url: /ru/net/create-rectangular-torus-in-3d-scene/
description: Используя Aspose.3D for .NET API, разработчики могут создавать объекты 3D, а затем сохранять сцену 3D в любом поддерживаемом формате 3D.
---
{{% alert color="primary" %}} 

Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, разработчики могут создавать объекты 3D, а затем сохранять сцену 3D в любом поддерживаемом формате 3D.

{{% /alert %}} 
##  **Прямоугольный тор**
Мы добавили класс `RectangularTorus`, он позволяет разработчикам поместить в сцену параметризованный прямоугольный тор, который может быть преобразован в порядковый сетчатый/треугольный сетчатый во время сохранения сцены в различные поддерживаемые форматы файлов.

**C#**

{{< highlight "java" >}}

 RectangularTorus rt = new RectangularTorus();

rt.InnerRadius = 17;

rt.OuterRadius = 22;

rt.Height = 30;

rt.Arc = Math.PI * 0.5;

Scene scene = new Scene();

scene.RootNode.CreateChildNode(rt);

scene.Save("rtorus.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

Сгенерированный прямоугольный тор выглядит следующим образом:

! [Для: имаге_альт_текст](create-rectangular-torus-in-3d-scene_1.png)
