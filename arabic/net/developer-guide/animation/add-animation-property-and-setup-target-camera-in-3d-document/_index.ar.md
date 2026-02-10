---
title: إضافة خاصية الرسوم المتحركة وإعداد الكاميرا المستهدفة في مستند 3D
type: docs
weight: 10
url: /ar/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: في Aspose.3D ، الرسوم المتحركة للكائن هي في الواقع رسوم متحركة بإطار رئيسي يتم حركتها على الخصائص. لتنشيط الخصائص ، تحتاج إلى مثيل انحناء يحدد مكونات خاصية إلى منحنيات مختلفة ، على سبيل المثال ، يمكن أن تحتوي خاصية Vector3 على 3 مكونات X/Y/Z ، والتي ستضع ثلاث قنوات في رسم الخرائط المنحنية ، يمكن أن تحتوي كل قناة على مجموعة من المنحنيات.
---
##  **إضافة خاصية الرسوم المتحركة في مستند 3D**
Aspose.3D for .NET يدعم عرض مشهد متحرك. تشرح هذه المقالة المتطلبات الأساسية لنقل كائن ما.
###  **Sition ove sition sition sition**
{{% alert color="primary" %}}

كائن الفئة [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) قيد الاستخدام في الرمز. يمكننا [إنشاء كائن فئة Mesh كما روى هناك](/3d/ar/net/create-and-read-an-existing-3d-scene/) ويجب أن نتحرك خاصية الترجمة المحلية للعقدة أيضًا: [Aدينغ رانسوفورميشن إلى oode](/3d/ar/net/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D, object animation is actually key-frame animation that animates on properties. To animate properties, you need a `CurveMapping` instance which maps components of a property to different curves, for example, a `Vector3` property can have 3 components `X`/`Y`/`Z`, which will set up three channels in `CurveMapping`, every channel can have a set of `Curve`.

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
##  **إعداد الكاميرا المستهدفة في ملف 3D**
Aspose.3D for .NET عروض لإعداد الكاميرا المستهدفة في ملف 3D. في بعض تنسيقات الملفات ، يدعم الضوء/الكاميرا الهدف ، مما يسمح للضوء/الكاميرا دائمًا بمواجهة عقدة محددة ، وهذا مفيد في الرسوم المتحركة.

{{% alert color="primary" %}}

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) and [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) classes are being used in the code. To save a `Scene`, [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) method is being used, it accepts a file name with complete path and [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat) parameter.

{{% /alert %}}

في المثال أدناه ، تم إعداد الهدف والكاميرا في ملف 3D:

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
