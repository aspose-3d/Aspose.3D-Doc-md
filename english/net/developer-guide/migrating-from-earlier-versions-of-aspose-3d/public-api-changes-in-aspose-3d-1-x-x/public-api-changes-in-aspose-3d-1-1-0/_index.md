---
title: Public API Changes in Aspose.3D 1.1.0
type: docs
weight: 60
url: /net/public-api-changes-in-aspose-3d-1-1-0/
---

**Contents Summary**

- [FBX7200ASCII Saving Option is added in the FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [FBX7200Binary Saving Option is added in the FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [FBX7300ASCII Saving Option is added in the FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [FBX7300Binary Saving Option is added in the FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [WavefrontOBJ Saving Option is added in the FileFormat and FileFormatType](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 1.0.0 to 1.1.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
### **FBX7200ASCII Saving Option is added in the FileFormat**
The FBX7200ASCII format option has been added in the FileFormat enum. It represents ASCII FBX file format, with 7.2.0 version. Example code:

**C#**

{{< highlight csharp >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

### **FBX7200Binary Saving Option is added in the FileFormat**
The FBX7200Binary format option has been added in the FileFormat enum. It represents Binary FBX file format, with 7.2.0 version. Example code:

**C#**

{{< highlight csharp >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

### **FBX7300ASCII Saving Option is added in the FileFormat**
The FBX7300ASCII format option has been added in the FileFormat enum. It represents ASCII FBX file format, with 7.3.0 version. Example code:

**C#**

{{< highlight csharp >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

### **FBX7300Binary Saving Option is added in the FileFormat**
The FBX7300Binary format option has been added in the FileFormat enum. It represents Binary FBX file format, with 7.3.0 version. Example code:

**C#**

{{< highlight csharp >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

### **WavefrontOBJ Saving Option is added in the FileFormat and FileFormatType**
The WavefrontOBJ format option has been added in the FileFormat and FileFormatType enums. It represents Wavefront’s Obj file format. Example code:

**C#**

{{< highlight csharp >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

