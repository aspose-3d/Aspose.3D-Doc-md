---
title: Настройте конверсию материалов Non-PBR в PBR перед сохранением 3D сцены в формат GLTF 2,0 в C#
linktitle: Настройте конверсию материалов Non-PBR в PBR перед сохранением сцены 3D в формат GLTF 2,0
type: docs
weight: 70
url: /ru/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Класс сцены Aspose.3D API представляет собой сцену 3D. Разработчики уже могут построить сцену 3D, добавив различные объекты. GLTF 2,0 поддерживает только материалы PBR (физическое отображение), Aspose.3D API внутренне преобразует материалы, не относящиеся к PBR, в материалы PBR перед экспортом в GLTF 2,0.
---
{{% alert color="primary" %}} 

Класс [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) API представляет собой сцену 3D. Разработчики уже могут построить сцену 3D, добавив различные объекты. GLTF 2,0 поддерживает только материалы PBR (физическое отображение), Aspose.3D API внутренне преобразует материалы, не относящиеся к PBR, в материалы PBR перед экспортом в GLTF 2,0 (материалы в сцене останутся неизменными во время экспорта), и разработчики могут предоставить настраиваемую функцию преобразования для переопределения поведения по умолчанию.

{{% /alert %}} 
## **Преобразование материала Non-PBR в PBR**
Этот пример кода C# демонстрирует, как преобразовать материал в материал PBR, а затем сохраняет сцену 3D в формате GLTF с помощью C# 3D манипуляции с файлами и преобразования API:

**C#**

{{< highlight "java" >}}

 // initialize a new 3D scene

var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = delegate(Material material)

{

    PhongMaterial m = (PhongMaterial) material;

    return new PbrMaterial() {Albedo = new Vector3(m.DiffuseColor.x, m.DiffuseColor.y, m.DiffuseColor.z)};

};

// save in GLTF 2.0 format

s.Save("test.gltf", opt);

{{< /highlight >}}
