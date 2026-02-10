---
title: احفظ مستند 3D بتنسيقات مختلفة 3D باستخدام C#
linktitle: توفير مستند 3D
type: docs
weight: 20
url: /ar/net/save-a-3d-document/
description: فئة المشهد لـ Aspose. يمثل 3D API مستند 3D ويمكن للمطورين حفظ الكائن الخاص به بأي تنسيق ملف مدعوم.
---
##  **Oفيرفيو**
توضح المقالة كيف يمكنك حفظ مستند 3D بتنسيقات مختلفة باستخدام مكتبة معالجة المستندات C# 3D ، بما في ذلك

- توفير مستند 3D بتنسيق FBX باستخدام C# - AutoDesk
- وفِّر مستند 3D بتنسيق DAE باستخدام C# - Collada
- وفر مستند 3D بتنسيق 3DS باستخدام C# - Discreet 3D Studio
- وفِّر مستند 3D بتنسيق DRC باستخدام C# - Google Draco

{{% alert color="primary" %}} 

فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) من Aspose. يمثل 3D API مستند 3D ويمكن للمطورين حفظ الكائن الخاص به بأي تنسيق ملف مدعوم. لحفظ مشهد 3D ، ما عليك سوى استخدام طريقة [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) ، فهي تقبل اسم ملف بمسار كامل أو كائن دفق ملف. Aspose.3D API يقدم معلمة `FileFormat` أخرى لتحديد تنسيق ملف الإخراج.

{{% /alert %}} 

##  **توفير مشهد 3D بتنسيقات 3D المدعومة**

تُظهر عينة الرمز C# أدناه كيفية حفظ مشهد أو مستند 3D في تدفق بتنسيقات مختلفة مدعومة من 3D.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
// Load a 3D document into Aspose.3D
Scene scene = new Scene();

// Open an existing 3D scene
scene.Open("document.fbx");

// Save Scene to a stream
MemoryStream dstStream = new MemoryStream();
scene.Save(dstStream, FileFormat.FBX7500ASCII);
            
// Save Scene to a local path
scene.Save("output_out.fbx");

{{< /highlight >}}
