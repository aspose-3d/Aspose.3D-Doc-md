---
title: اكتشاف تنسيق ملف 3D
type: docs
weight: 10
url: /ar/java/detect-format-of-3d-file/
description: Aspose.3D for Java API يدعم اكتشاف تنسيقات 3D المدعومة قبل الفتح لأن امتداد الملف لا يضمن أن محتوى الملف مناسب.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API يدعم اكتشاف تنسيقات 3D المدعومة قبل الفتح لأن امتداد الملف لا يضمن أن محتوى الملف مناسب.

{{% /alert %}} 
##  **Detect orormat roقواعد اللغة ple وافرة**
Tرمز المصدر يوضح كيفية الكشف عن تنسيق الملف (باستخدام مسار الملف أو تيار) والتحقق من امتداده.

{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// detect format of 3D file
FileFormat inputFormat = FileFormat.detect(MyDir + "document.fbx");
// display the file format
System.out.println("File Format: " + inputFormat.toString());
{{< /highlight >}}




