---
title: إنشاء مشهد بأشكال بدائية 3D
type: docs
weight: 20
url: /ar/java/create-scene-with-primitive-3d-shapes/
description: Aspose.3D for Java API يدعم الأشكال الأولية 3D. سيتم تحويل جميع البارامترات الأولية إلى شبكة تلقائيًا مع الحفظ بأي تنسيق ملف إخراج مدعوم.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API يدعم الأشكال الأولية 3D. سيتم تحويل جميع البارامترات الأولية إلى شبكة تلقائيًا مع الحفظ بأي تنسيق ملف إخراج مدعوم.

{{% /alert %}} 
##  **بناء مشهد من أشكال بدائية 3D**
Modeling is the process of pure creation and Aspose.3D API supports creating a scene with primitive 3D shapes.
###  **Pروغرامينغ ple وافرة**
هذا المثال البرمجي يُنشئ مشهد بأشكال 3D بدائية ويُحفظ في ملف FBX.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.getRootNode().createChildNode("box", new Box());
// Create a Cylinder model
scene.getRootNode().createChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
MyDir = MyDir + RunExamples.getOutputFilePath("test.fbx");
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
