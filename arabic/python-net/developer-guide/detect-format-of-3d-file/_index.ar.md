---
title: اكتشاف تنسيق ملف 3D
type: docs
weight: 10
url: /ar/python-net/detect-format-of-3d-file/
description: باستخدام Aspose.3D for Python via .NET API ، قد يكتشف المطورون تنسيق ملفات 3D المدعومة قبل فتحها لأن ملحق الملف لا يضمن أن محتوى الملف مناسب.
---
{{% alert color="primary" %}} 

باستخدام Aspose.3D for Python via .NET API ، قد يكتشف المطورون تنسيق ملفات 3D المدعومة قبل فتحها لأن ملحق الملف لا يضمن أن محتوى الملف مناسب.

{{% /alert %}} 
##  **Detect orormat roقواعد اللغة ple وافرة**
Tانه يتبع رمز العينة يوضح كيفية الكشف عن تنسيق ملف (باستخدام مسار الملف أو تيار) والتحقق من امتداده.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# Detect the format of a 3D file
inputFormat = a3d.FileFormat.detect("document.fbx");
# Display the file format
print("File Format: " + str(inputFormat))

{{< /highlight >}}
