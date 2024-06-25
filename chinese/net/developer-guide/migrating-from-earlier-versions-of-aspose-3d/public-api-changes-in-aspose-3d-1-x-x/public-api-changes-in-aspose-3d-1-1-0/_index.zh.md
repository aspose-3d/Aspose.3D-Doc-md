---
title: Aspose.3D 1.1.0中的公共 API 更改
type: docs
weight: 60
url: /zh/net/public-api-changes-in-aspose-3d-1-1-0/
---
**内容摘要**

- [文件格式中添加了FBX7200ASCII保存选项](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [文件格式中添加了fbx7200二进制保存选项](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [文件格式中添加了FBX7300ASCII保存选项](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [文件格式中添加了fbx7300二进制保存选项](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [在FileFormat和FileFormatType中添加了 WavefrontOBJ 保存选项](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

本文档介绍了对 Aspose.3D API 从版本1.0.0到1.1.0的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.3D 中幕后行为的任何更改的描述。

{{% /alert %}} 
###  **文件格式中添加了FBX7200ASCII保存选项**
FileFormat枚举中添加了FBX7200ASCII格式选项。它表示ASCII FBX 文件格式，版本为7.2.0。示例代码:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

###  **文件格式中添加了fbx7200二进制保存选项**
在FileFormat枚举中添加了FBX7200Binary格式选项。它表示7.2.0版本的二进制 FBX 文件格式。示例代码:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

###  **文件格式中添加了FBX7300ASCII保存选项**
FileFormat枚举中添加了FBX7300ASCII格式选项。它表示ASCII FBX 文件格式，版本为7.3.0。示例代码:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

###  **文件格式中添加了fbx7300二进制保存选项**
在FileFormat枚举中添加了FBX7300Binary格式选项。它表示7.3.0版本的二进制 FBX 文件格式。示例代码:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

###  **在FileFormat和FileFormatType中添加了 WavefrontOBJ 保存选项**
WavefrontOBJ 格式选项已添加到FileFormat和FileFormatType枚举中。它表示 Wavefront 的Obj文件格式。示例代码:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

