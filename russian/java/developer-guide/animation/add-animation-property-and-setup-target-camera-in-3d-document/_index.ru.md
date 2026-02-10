---
title: Добавить свойство анимации и настройку целевой камеры в документе 3D
type: docs
weight: 10
url: /ru/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java поддерживает рендеринг анимированной сцены. Эта статья объясняет предпосылки для перемещения объекта.
---
##  **Добавить свойство анимации в документе 3D**
Aspose.3D for Java поддерживает рендеринг анимированной сцены. Эта статья объясняет предпосылки для перемещения объекта.
###  **Положение Move Cube**
{{% alert color="primary" %}}

В коде используется объект класса `Mesh`. Мы можем [Создать объект класса Mesh, как там рассказано](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/), и он также должен анимировать свойство локального перевода узла: [Добавление преобразования к узлу](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

В Aspose.3D for Java API экземпляр анимации на самом деле является анимацией ключевого кадра, которая анимируется в свойствах. Чтобы анимировать свойства, вам нужен экземпляр `CurveMapping`, который отображает компоненты свойства на разные кривые, например, свойство `Vector3` может иметь 3 компонента `X`/`Y`/`Z`, который настроит три канала за `CurveMapping`, каждый канал может иметь набор `Curve`.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize scene object
Scene scene = new Scene();

// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();

// Each cube node has their own translation
Node cube1 = scene.getRootNode().createChildNode("cube1", mesh);

// Find translation property on node's transform object
Property translation = cube1.getTransform().findProperty("Translation");

// Create a bind point based on translation property
BindPoint bindPoint = new BindPoint(scene, translation);

// Create the animation curve on X component of the scale
KeyframeSequence kfs = new KeyframeSequence();
// Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
kfs.add(0, 10.0f, Interpolation.BEZIER);
// Move node's translation to (20, 0, -10) at 3 sec
kfs.add(3, 20.0f, Interpolation.BEZIER);
// Move node's translation to (30, 0, 0) at 5 sec
kfs.add(5, 30.0f, Interpolation.LINEAR);
            
bindPoint.bindKeyframeSequence("X", kfs);

kfs = new  KeyframeSequence();
// Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
kfs.add(0, 10.0f, Interpolation.BEZIER);
// Move node's translation to (20, 0, -10) at 3 sec
kfs.add(3, -10.0f, Interpolation.BEZIER);
// Move node's translation to (30, 0, 0) at 5 sec
kfs.add(5, 0.0f, Interpolation.LINEAR);
            
bindPoint.bindKeyframeSequence("Z", kfs);

// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("PropertyToDocument.fbx");

// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);

{{< /highlight >}}
##  **Настройте целевую камеру в файле 3D**
Aspose.3D for Java предлагает настроить целевую камеру в файле 3D. В некоторых форматах файлов свет/камера поддерживает цель, что позволяет свету/камере всегда смотреть на указанный узел, это полезно в анимации.

{{% alert color="primary" %}}

В коде используются классы `Scene`, `Camera`, `Node` и `Transform`. Чтобы сэкономить `Scene`, используется метод `Scene.save`, он принимает имя файла с полным путем и параметром `FileFormat`.

{{% /alert %}}

В примере ниже цель и камера настроены в файле 3D:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize scene object
Scene scene = new Scene();
// Get a child node object
Node cameraNode = scene.getRootNode().createChildNode("camera", new Camera());
// Set camera node translation
cameraNode.getTransform().setTranslation(new Vector3(100, 20, 0));
((Camera)cameraNode.getEntity()).setTarget(scene.getRootNode().createChildNode("target"));
MyDir = MyDir + "camera-test.3ds";
scene.save(MyDir, FileFormat.DISCREET3DS);
{{< /highlight >}}
