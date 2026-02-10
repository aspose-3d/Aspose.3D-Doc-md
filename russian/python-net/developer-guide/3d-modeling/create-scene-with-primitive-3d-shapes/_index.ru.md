---
title: Создайте сцену с примитивными формами 3D
type: docs
weight: 10
url: /ru/python-net/create-scene-with-primitive-3d-shapes/
description: Используя Aspose.3D for Python via .NET, разработчики могут определить сцену с примитивными 3D формами. Все параметризованные примитивы будут автоматически преобразованы в mesh при сохранении в любом поддерживаемом формате выходного файла.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), разработчики могут определить сцену с примитивными 3D формами. Все параметризованные примитивы будут автоматически преобразованы в mesh при сохранении в любом поддерживаемом формате выходного файла.

{{% /alert %}}
##  **Построить сцену из примитивных 3D фигур**
Моделирование-это процесс чистого создания и Aspose.3D API поддерживает создание сцены с примитивными 3D формами.
###  **Образец программирования**
В этом примере кода создается сцена с примитивными фигурами 3D и сохраняется в файле FBX.

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Box, Cylinder

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
#  Initialize a Scene object
scene = Scene()
#  Create a Box model
scene.root_node.create_child_node("box", Box())
#  Create a Cylinder model
scene.root_node.create_child_node("cylinder", Cylinder())
#  Save drawing in the FBX format
output = "out"  + "test.fbx"
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
