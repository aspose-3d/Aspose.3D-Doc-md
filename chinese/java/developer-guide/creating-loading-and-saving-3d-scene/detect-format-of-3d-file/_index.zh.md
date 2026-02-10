---
title: 检测 3D 文件的格式
type: docs
weight: 10
url: /zh/java/detect-format-of-3d-file/
description: Aspose.3D for Java API 支持在打开之前检测 3D 支持的格式，因为文件扩展名不能保证文件内容正确。
---
{{% alert color="primary" %}} 

Aspose.3D for Java API 支持在打开之前检测 3D 支持的格式，因为文件扩展名不能保证文件内容正确。

{{% /alert %}} 
##  **检测格式编程示例**
此源代码说明了如何检测文件格式 (使用文件路径或流) 并检查其扩展名。

{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// detect format of 3D file
FileFormat inputFormat = FileFormat.detect(MyDir + "document.fbx");
// display the file format
System.out.println("File Format: " + inputFormat.toString());
{{< /highlight >}}




