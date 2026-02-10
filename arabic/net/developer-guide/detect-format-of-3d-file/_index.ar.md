---
title: اكتشاف تنسيق ملف 3D في C# .NET
linktitle: اكتشاف تنسيق ملف 3D
type: docs
weight: 10
url: /ar/net/detect-format-of-3d-file/
description: باستخدام Aspose.3D for .NET API ، قد يكتشف المطورون تنسيق ملفات 3D المدعومة في C# قبل فتحها لأن ملحق الملف لا يضمن أن محتوى الملف مناسب.
---
{{% alert color="primary" %}} 

باستخدام Aspose.3D for .NET API ، قد يكتشف المطورون تنسيق ملفات 3D المدعومة في C# قبل فتحها لأن ملحق الملف لا يضمن أن محتوى الملف مناسب.

{{% /alert %}} 
##  **Detect orormat roقواعد اللغة ple وافرة**
يوضح رمز عينة C# التالي كيفية اكتشاف تنسيق ملف من ملف 3D (باستخدام مسار الملف أو الدفق) والتحقق من امتداده.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Detect the format of a 3D file
FileFormat inputFormat = FileFormat.Detect("document.fbx");
// Display the file format
Console.WriteLine("File Format: " + inputFormat.ToString());

{{< /highlight >}}
