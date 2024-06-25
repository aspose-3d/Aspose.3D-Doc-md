---
title: Настройте преобразование материалов без PBR в PBR перед сохранением 3D сцен в формате GLTF 2,0 в C#
linktitle: Настройте преобразование материалов без PBR в PBR перед сохранением сцен 3D в формат GLTF 2,0
type: docs
weight: 70
url: /ru/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Класс Сцена Aspose.3D API представляет собой сцену 3D. Разработчики уже могут построить сцену 3D, добавив различные сущности. GLTF 2,0 поддерживает только материалы PBR (физический рендеринг), Aspose.3D API внутренне преобразует материалы, не являющиеся PBR, в материалы PBR перед экспортом в GLTF 2,0.
---
{{% alert color="primary" %}} 

Класс [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) из Aspose.3D API представляет сцену 3D. Разработчики уже могут построить сцену 3D, добавив различные сущности. GLTF 2,0 поддерживает только материалы PBR (физический рендеринг), Aspose.3D API внутренне преобразует материалы, не являющиеся PBR, в материалы PBR перед экспортом в GLTF 2,0 (материалы в сцене останутся неизменными во время экспорта), и разработчики могут предоставить пользовательскую функцию преобразования для переопределения поведения по умолчанию.

{{% /alert %}} 
##  **Преобразование материала Non-PBR в PBR**
Этот пример кода C# демонстрирует, как преобразовать материал в материал PBR, а затем сохранить сцену 3D в формате GLTF с манипуляциями с файлами C# 3D и конвертацией API:

**C#**

{{< highlight "java" >}}

 // initialize a new 3D scene

var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = (Material material) => {
    var pbr = PbrMaterial.FromMaterial(material);
    //customize your own PBR material here, you can get the original OBJ's material from the parameter mat.
    //to create a compatible material with obj2gltf, use following definition:
    pbr.MetallicFactor = 0;
    pbr.RoughnessFactor = 0.98;
    return pbr;
};

// save in GLTF 2.0 format

s.Save("test.gltf", opt);

{{< /highlight >}}


##  **Ресурсы**

1. [Онлайн учебник](https://products.aspose.com/3d/tutorial/use-phong-material-to-pbr-material/)
