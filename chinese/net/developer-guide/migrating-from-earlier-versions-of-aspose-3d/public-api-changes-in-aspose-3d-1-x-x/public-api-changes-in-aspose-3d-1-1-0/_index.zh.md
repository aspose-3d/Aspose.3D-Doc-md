---
title: Aspose.3D中的公共API变化1.1.0
type: docs
weight: 60
url: /zh/net/public-api-changes-in-aspose-3d-1-1-0/
---
**内容摘要**

- [文件格式中添加了FBX7200ASCII保存选项](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [文件格式中添加了fbx7200二进制保存选项](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [文件格式中添加了FBX7300ASCII保存选项](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [文件格式中添加了fbx7300二进制保存选项](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [在文件格式和文件格式类型中添加了WavefrontOBJ保存选项](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

本文档介绍了Aspose.3D API从1.0.0版到1.1.0版的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对Aspose.3D幕后行为的任何变化的描述。

{{% /alert %}} 
### **文件格式中添加了FBX7200ASCII保存选项**
文件格式枚举中添加了FBX7200ASCII格式选项。它代表ASCII FBX的文件格式，与7.2.0版本。示例代码:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

### **文件格式中添加了fbx7200二进制保存选项**
文件格式枚举中添加了fbx7200二进制格式选项。它代表二进制FBX文件格式，与7.2.0版本。示例代码:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

### **文件格式中添加了FBX7300ASCII保存选项**
文件格式枚举中添加了FBX7300ASCII格式选项。它代表ASCII FBX的文件格式，与7.3.0版本。示例代码:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

### **文件格式中添加了fbx7300二进制保存选项**
文件格式枚举中添加了fbx7300二进制格式选项。它代表二进制FBX文件格式，与7.3.0版本。示例代码:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

### **在文件格式和文件格式类型中添加了WavefrontOBJ保存选项**
已在FileFormat和FileFormatType枚举中添加了WavefrontOBJ格式选项。它表示Wavefront的Obj文件格式。示例代码:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

