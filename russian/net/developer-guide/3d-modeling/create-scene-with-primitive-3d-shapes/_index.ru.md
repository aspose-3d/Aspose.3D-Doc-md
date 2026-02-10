---
title: Создайте сцену с примитивными формами 3D
type: docs
weight: 10
url: /ru/net/create-scene-with-primitive-3d-shapes/
description: Используя Aspose.3D for .NET, разработчики могут определить сцену с примитивными фигурами 3D. Все параметризованные примитивы будут автоматически преобразованы в mesh при сохранении в любом поддерживаемом формате выходного файла.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/), разработчики могут определить сцену с примитивными 3D формами. Все параметризованные примитивы будут автоматически преобразованы в mesh при сохранении в любом поддерживаемом формате выходного файла.

{{% /alert %}}
##  **Построить сцену из примитивных 3D фигур**
Моделирование-это процесс чистого создания и Aspose.3D API поддерживает создание сцены с примитивными 3D формами.
###  **Образец программирования**
В этом примере кода создается сцена с примитивными фигурами 3D и сохраняется в файле FBX.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.RootNode.CreateChildNode("box", new Box());
// Create a Cylinder model
scene.RootNode.CreateChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
scene.Save("test.fbx");


{{< /highlight >}}
