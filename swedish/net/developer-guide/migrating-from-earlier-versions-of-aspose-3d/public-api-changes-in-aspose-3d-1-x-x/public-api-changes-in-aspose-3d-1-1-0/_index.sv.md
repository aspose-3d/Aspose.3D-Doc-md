---
title: Offentlig API Förändringar Aspose.3D 1,1,0
type: docs
weight: 60
url: /sv/net/public-api-changes-in-aspose-3d-1-1-0/
---
**Innehåll**

- [FBX7200ASCII sparalternativ läggs till i FileFormatt](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [FBX7200Binary sparalternativ läggs till i FileFormatt](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [FBX7300ASCII sparalternativ läggs till i filformatet](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [FBX7300Binary sparalternativ läggs till i FileFormatt](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [WavefrontOBJ Spara alternativet läggs till i FilFormat och FileFormatTypeName](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

Detta dokument beskriver ändringar av Aspose.3D API från version 1.0.0 till 1.1. 0, som kan vara av intresse för modul / applikationsutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteende bakom kulisserna i Aspose.3D.

{{% /alert %}} 
### **FBX7200ASCII sparalternativ läggs till i FileFormatt**
Alternativet FBX7200ASCII format har lagts till i FileFormat enum. Den representerar ASCII FBX filformat, med 7.2.0 version. Exempelkod:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

### **FBX7200Binary sparalternativ läggs till i FileFormatt**
Alternativet FBX7200Binary format har lagts till i FileFormat enum. Den representerar Binary FBX filformat, med 7.2.0 version. Exempelkod:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

### **FBX7300ASCII sparalternativ läggs till i filformatet**
Alternativet FBX7300ASCII format har lagts till i FileFormat enum. Den representerar ASCII FBX filformat, med 7.3.0 version. Exempelkod:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

### **FBX7300Binary sparalternativ läggs till i FileFormatt**
Alternativet FBX7300Binary format har lagts till i FileFormat enum. Den representerar Binary FBX filformat, med 7.3.0 version. Exempelkod:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

### **WavefrontOBJ Spara alternativet läggs till i FilFormat och FileFormatTypeName**
Alternativet WavefrontOBJ format har lagts till i FileFormat och FileFormatType enums. Den representerar Wavefront's Obj filformat. Exempelkod:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

