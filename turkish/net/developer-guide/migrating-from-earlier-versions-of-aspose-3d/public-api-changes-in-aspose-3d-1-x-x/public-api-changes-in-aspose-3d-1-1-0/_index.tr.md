---
title: Kamu API Aspose içinde değişir. 3D 1.1.0
type: docs
weight: 60
url: /tr/net/public-api-changes-in-aspose-3d-1-1-0/
---
**Contents Summary**

- [Fleaving ption ption FileFormat eklenir](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [FiX7200Binary ving aving ption ption FileFormat eklenir](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [Fleaving ption ption FileFormat eklenir](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [FiX7300Binary ving aving ption ption FileFormat eklenir](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [Dosya biçiminde ve dosya biçiminde WavefrontOBJ kaydetme seçeneği eklenir](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 1.0.0 to 1.1.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Fleaving ption ption FileFormat eklenir**
Fbx7200ascii biçim seçeneği dosya biçiminde eklendi. 7.2.0 sürümü ile ascii FBX dosya formatını temsil eder. Örnek kod:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

###  **FiX7200Binary ving aving ption ption FileFormat eklenir**
Fileformat enum'a fbx7200binary format seçeneği eklendi. 7.2.0 sürümü ile ikili FBX dosya formatını temsil eder. Örnek kod:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

###  **Fleaving ption ption FileFormat eklenir**
Fbx7300ascii format seçeneği dosya biçiminde eklendi. 7.3.0 sürümü ile ascii FBX dosya formatını temsil eder. Örnek kod:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

###  **FiX7300Binary ving aving ption ption FileFormat eklenir**
Fileformat enum'a fbx7300binary format seçeneği eklendi. 7.3.0 sürümü ile ikili FBX dosya formatını temsil eder. Örnek kod:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

###  **Dosya biçiminde ve dosya biçiminde WavefrontOBJ kaydetme seçeneği eklenir**
The WavefrontOBJ format option has been added in the FileFormat and FileFormatType enums. It represents Wavefront’s Obj file format. Example code:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

