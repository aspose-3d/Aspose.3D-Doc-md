---
title: 检测 3D 文件的格式
type: docs
weight: 10
url: /zh/python-net/detect-format-of-3d-file/
description: 使用 Aspose.3D for Python via .NET API，开发人员可能会在打开受支持的 3D 文件之前检测到该文件的格式，因为文件扩展名不能保证文件内容是适当的。
---
{{% alert color="primary" %}} 

使用 Aspose.3D for Python via .NET API，开发人员可能会在打开受支持的 3D 文件之前检测到该文件的格式，因为文件扩展名不能保证文件内容是适当的。

{{% /alert %}} 
##  **检测格式编程示例**
下面的示例代码说明了如何检测文件格式 (使用文件路径或流) 并检查其扩展名。

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# Detect the format of a 3D file
inputFormat = a3d.FileFormat.detect("document.fbx");
# Display the file format
print("File Format: " + str(inputFormat))

{{< /highlight >}}
