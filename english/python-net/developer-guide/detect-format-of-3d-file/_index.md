---
title: Detect format of 3D file
type: docs
weight: 10
url: /python-net/detect-format-of-3d-file/
description: Using Aspose.3D for Python via .NET API, developers may detect the format of supported 3D files before opening it because the file extension does not guarantee that the file content is appropriate.
---

{{% alert color="primary" %}} 

Using Aspose.3D for Python via .NET API, developers may detect the format of supported 3D files before opening it because the file extension does not guarantee that the file content is appropriate.

{{% /alert %}} 
## **Detect Format Programming Sample**
The following sample code illustrates how to detect a file format (using the file path or stream) and check its extension.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# Detect the format of a 3D file
inputFormat = a3d.FileFormat.detect("document.fbx");
# Display the file format
print("File Format: " + str(inputFormat))
{{< /highlight >}}
