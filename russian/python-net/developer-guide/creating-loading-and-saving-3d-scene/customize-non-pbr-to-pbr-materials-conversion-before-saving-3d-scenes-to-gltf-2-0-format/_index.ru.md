---
title: Настройте конверсию материалов Non-PBR в PBR перед сохранением сцены 3D в формат GLTF 2,0
type: docs
weight: 70
url: /ru/python-net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Класс сцены Aspose.3D API представляет собой сцену 3D. Разработчики уже могут построить сцену 3D, добавив различные объекты. GLTF 2,0 поддерживает только материалы PBR (физическое отображение), Aspose.3D API внутренне преобразует материалы, не относящиеся к PBR, в материалы PBR перед экспортом в GLTF 2,0.
---
{{% alert color="primary" %}} 

Класс [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) API представляет собой сцену 3D. Разработчики уже могут построить сцену 3D, добавив различные объекты. GLTF 2,0 поддерживает только материалы PBR (физическое отображение), Aspose.3D API внутренне преобразует материалы, не относящиеся к PBR, в материалы PBR перед экспортом в GLTF 2,0 (материалы в сцене останутся неизменными во время экспорта), и разработчики могут предоставить настраиваемую функцию преобразования для переопределения поведения по умолчанию.

{{% /alert %}} 
## **Преобразование материала Non-PBR в PBR**
Этот пример кода демонстрирует, как преобразовать материал в материал PBR, а затем сохраняет сцену 3D в формате GLTF:

**C#**

```py

import aspose.threed as a3d

# initialize a new 3D scene

s = a3d.Scene()

box = a3d.Box()

mat = a3d.shading.PhongMaterial()
mat.diffuse_color = Vector3(1, 0, 1)

s.root_node.create_child_node("box1", box).material = mat

opt = a3d.formats.GLTFSaveOptions(FileFormat.GLTF2);

# save in GLTF 2.0 format

s.save("test.gltf", opt);

```
