---
title: Detect format of 3D file
type: docs
weight: 10
url: /java/detect-format-of-3d-file/
description: Aspose.3D for Java API has support of detecting 3D supported formats before opening because the file extension does not guarantee that the file content is appropriate.
---

{{% alert color="primary" %}} 

Aspose.3D for Java API has support of detecting 3D supported formats before opening because the file extension does not guarantee that the file content is appropriate.

{{% /alert %}} 
## **Detect Format Programming Sample**
This source code illustrates how to detect the file format (using the file path or stream) and check its extension.

{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// detect format of 3D file
FileFormat inputFormat = FileFormat.detect(MyDir + "document.fbx");
// display the file format
System.out.println("File Format: " + inputFormat.toString());
{{< /highlight >}}




