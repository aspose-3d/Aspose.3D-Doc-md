---
title: إنشاء مستند فارغ 3D
type: docs
weight: 20
url: /ar/java/create-an-empty-3d-document/
description: Aspose.3D for Java API يدعم إنشاء مشهد 3D من الصفر ، ثم التوفير بتنسيق 3D المدعوم.
---
##  **أنشئ مشهد 3D فارغ ووفر بتنسيق 3D المدعوم**
Aspose.3D for Java API يدعم إنشاء مشهد 3D من الصفر ، ثم التوفير بتنسيق 3D المدعوم.
###  **إنشاء مشهد فارغ 3D**
يرجى اتباع هذه الخطوات لإنشاء مشهد 3D مع Aspose.3D for Java API:

1. Rereate مثيل من**مشهد**فئة تمثل مشهد 3D.
1. توليد مستند 3D عن طريق الاتصال به**حفظ**طريقة من**مشهد**مثيل الصف.
####  **إنشاء مشهد 3D فارغ: عينات برمجة**
{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "document.fbx";
// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}




