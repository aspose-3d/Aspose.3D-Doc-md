---
title: توفير مستند 3D
type: docs
weight: 20
url: /ar/python-net/save-a-3d-document/
description: فئة المشهد لـ Aspose. يمثل 3D API مستند 3D ويمكن للمطورين حفظ الكائن الخاص به بأي تنسيق ملف مدعوم.
---
{{% alert color="primary" %}} 

فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) من Aspose. يمثل 3D API مستند 3D ويمكن للمطورين حفظ الكائن الخاص به بأي تنسيق ملف مدعوم. لحفظ مشهد 3D ، ما عليك سوى استخدام طريقة [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) ، فهي تقبل اسم ملف بمسار كامل أو كائن دفق ملف. Aspose.3D API يقدم معلمة `FileFormat` أخرى لتحديد تنسيق ملف الإخراج.

{{% /alert %}} 
##  **وفِّر مشهد 3D**


Tانه رمز عينة أدناه يظهر كيفية حفظ وثيقة إلى تيار.

{{< highlight "python" >}}
import aspose.threed as a3d
import io
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
# Load a 3D document into Aspose.3D
scene = a3d.Scene.from_file("document.fbx")

# Save Scene to a stream
dstStream = io.BytesIO()
scene.save(dstStream, a3d.FileFormat.FBX7500ASCII);

{{< /highlight >}}
