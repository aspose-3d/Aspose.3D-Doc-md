---
title: Public API Changes Aspose.3D 1.1.0
type: docs
weight: 60
url: /tr/net/public-api-changes-in-aspose-3d-1-1-0/
---
**Contents Summary**

- [Fleaving ption ption FileFormat eklenir](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [FiX7200Binary ving aving ption ption FileFormat eklenir](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [Fleaving ption ption FileFormat eklenir](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [FiX7300Binary ving aving ption ption FileFormat eklenir](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [FileFormat ve FileFormatType içinde WavefrontOBJ ving aving ption ption eklenir](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

This belgesi, 1.0.0 sürümünden 1.1.0 'a kadar Aspose.3D API 'teki değişiklikleri açıklar, bu modül/uygulama geliştiricilerine ilgi gösterebilir. It sadece yeni ve güncellenmiş kamu yöntemlerini değil, aynı zamanda Aspose.3D 'deki sahnelerin arkasındaki davranıştaki herhangi bir değişikliğin açıklamasını da içerir.

{{% /alert %}} 
### **Fleaving ption ption FileFormat eklenir**
He he format format seçeneği FileFormat enum'a eklendi. It 7.2.0 sürümü ile ASCII FBX dosya formatını temsil eder. Example kodu:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

### **FiX7200Binary ving aving ption ption FileFormat eklenir**
He he FX77200Binary format seçeneği File. ormat enum'a eklendi. It, 7.2.0 sürümü ile FBX dosya formatını temsil eder. Example kodu:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

### **Fleaving ption ption FileFormat eklenir**
He he format format seçeneği FileFormat enum'a eklendi. It 7.3.0 sürümü ile ASCII FBX dosya formatını temsil eder. Example kodu:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

### **FiX7300Binary ving aving ption ption FileFormat eklenir**
He he FX77300Binary format seçeneği File. ormat enum'a eklendi. It, 7.3.0 sürümü ile FBX dosya formatını temsil eder. Example kodu:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

### **FileFormat ve FileFormatType içinde WavefrontOBJ ving aving ption ption eklenir**
Fhe WavefrontOBJ format seçeneği, File. ormat ve File. ormat. ype enumlarına eklenmiştir. It Wavefront'in Obj dosya formatını temsil eder. Example kodu:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

