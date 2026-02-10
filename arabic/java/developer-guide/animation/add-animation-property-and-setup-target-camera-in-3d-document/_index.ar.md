---
title: إضافة خاصية الرسوم المتحركة وإعداد الكاميرا المستهدفة في مستند 3D
type: docs
weight: 10
url: /ar/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java يدعم عرض مشهد متحرك. تشرح هذه المقالة المتطلبات الأساسية لنقل كائن ما.
---
##  **إضافة خاصية الرسوم المتحركة في مستند 3D**
Aspose.3D for Java يدعم عرض مشهد متحرك. تشرح هذه المقالة المتطلبات الأساسية لنقل كائن ما.
###  **Sition ove sition sition sition**
{{% alert color="primary" %}}

كائن الفئة `Mesh` قيد الاستخدام في الرمز. يمكننا [إنشاء كائن فئة Mesh كما روى هناك](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) ويجب أن نتحرك خاصية الترجمة المحلية للعقدة أيضًا: [Aدينغ رانسوفورميشن إلى oode](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D for Java API, animation instance is actually key-frame animation that animates on properties. In order animate properties, you need a `CurveMapping` instance which maps components of a property to different curves, for example, a `Vector3` property can have 3 components `X`/`Y`/`Z`, which will set up three channels in `CurveMapping`, every channel can have a set of `Curve`.

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
##  **إعداد الكاميرا المستهدفة في ملف 3D**
Aspose.3D for Java عروض لإعداد الكاميرا المستهدفة في ملف 3D. في بعض تنسيقات الملفات ، يدعم الضوء/الكاميرا الهدف ، مما يسمح للضوء/الكاميرا دائمًا بمواجهة عقدة محددة ، وهذا مفيد في الرسوم المتحركة.

{{% alert color="primary" %}}

The `Scene`, `Camera`, `Node` and `Transform` classes are being used in the code. in order to save a `Scene`, `Scene.save` method is being used, it accepts a file name with complete path and `FileFormat` parameter.

{{% /alert %}}

في المثال أدناه ، تم إعداد الهدف والكاميرا في ملف 3D:

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
