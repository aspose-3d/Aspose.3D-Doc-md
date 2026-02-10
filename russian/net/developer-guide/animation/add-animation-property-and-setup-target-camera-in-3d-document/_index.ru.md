---
title: Добавить свойство анимации и настройку целевой камеры в документе 3D
type: docs
weight: 10
url: /ru/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: В Aspose.3D объектная анимация на самом деле является ключевой анимацией кадра, которая анимируется в свойствах. Чтобы анимировать свойства, вам нужен экземпляр CurveMapping, который отображает компоненты свойства на различные кривые, например, свойство Vector3 может иметь 3 компонента X/Y/Z, которые будут настраивать три канала в CurveMapping, каждый канал может иметь набор кривых.
---
##  **Добавить свойство анимации в документе 3D**
Aspose.3D for .NET поддерживает рендеринг анимированной сцены. Эта статья объясняет предпосылки для перемещения объекта.
###  **Положение Move Cube**
{{% alert color="primary" %}}

В коде используется объект класса [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh). Мы можем [Создать объект класса Mesh, как там рассказано](/3d/ru/net/create-and-read-an-existing-3d-scene/), и он также должен анимировать свойство локального перевода узла: [Добавление преобразования к узлу](/3d/ru/net/adding-transformation-to-the-node/).

{{% /alert %}}

В Aspose.3D объектная анимация на самом деле является ключевой анимацией кадра, которая анимируется в свойствах. Чтобы анимировать свойства, вам нужен экземпляр `CurveMapping`, который отображает компоненты свойства на разные кривые, например, свойство `Vector3` может иметь 3 компонента `X`/`Y`/`Z`, который настроит три канала за `CurveMapping`, каждый канал может иметь набор `Curve`.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();             

// Each cube node has their own translation
Node cube1 = scene.RootNode.CreateChildNode("cube1", mesh);

// Find translation property on node's transform object
Property translation = cube1.Transform.FindProperty("Translation");
            
// Create a bind point based on translation property
BindPoint bindPoint = new BindPoint(scene, translation);

// Create the animation curve on X component of the scale 
bindPoint.BindKeyframeSequence("X", new KeyframeSequence()
{
    // Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
    {0, 10.0f, Interpolation.Bezier},
    // Move node's translation to (20, 0, -10) at 3 sec
    {3, 20.0f, Interpolation.Bezier},
    // Move node's translation to (30, 0, 0) at 5 sec
    {5, 30.0f, Interpolation.Linear},
});

// Create the animation curve on Z component of the scale 
bindPoint.BindKeyframeSequence("Z", new KeyframeSequence()
{
    // Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
    {0, 10.0f, Interpolation.Bezier},
    // Move node's translation to (20, 0, -10) at 3 sec
    {3, -10.0f, Interpolation.Bezier},
    // Move node's translation to (30, 0, 0) at 5 sec
    {5, 0.0f, Interpolation.Linear},
});

// Save 3D scene in the supported file formats
scene.Save("PropertyToDocument.fbx");

{{< /highlight >}}
##  **Настройте целевую камеру в файле 3D**
Aspose.3D for .NET предлагает настроить целевую камеру в файле 3D. В некоторых форматах файлов свет/камера поддерживает цель, что позволяет свету/камере всегда смотреть на указанный узел, это полезно в анимации.

{{% alert color="primary" %}}

В коде используются классы [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) и [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform). Чтобы сохранить `Scene`, используется метод [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save), он принимает имя файла с полным путем и параметром [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat).

{{% /alert %}}

В примере ниже цель и камера настроены в файле 3D:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Get a child node object
Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());
// Set camera node translation
cameraNode.Transform.Translation = new Vector3(100, 20, 0);
cameraNode.GetEntity<Camera>().Target = scene.RootNode.CreateChildNode("target");
scene.Save("camera-test.3ds");

{{< /highlight >}}
