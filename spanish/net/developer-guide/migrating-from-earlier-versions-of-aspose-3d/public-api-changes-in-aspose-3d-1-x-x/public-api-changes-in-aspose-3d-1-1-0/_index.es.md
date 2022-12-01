---
title: Público API Cambios en Aspose.3D 1.1.0
type: docs
weight: 60
url: /es/net/public-api-changes-in-aspose-3d-1-1-0/
---
**Resumen de contenidos**

- [Se añade la opción de ahorro FBX7200ASCII en el formato de archivo](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [Se añade la opción de ahorro binario FBX7200en FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [Se añade la opción de ahorro FBX7300ASCII en el formato de archivo](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [Se añade la opción de ahorro binario FBX7300en FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [La opción de guardado WavefrontOBJ se agrega en FileFormat y FileFormatType](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.3D API de la versión 1.0.0 a 1.1.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.3D.

{{% /alert %}} 
### **Se añade la opción de ahorro FBX7200ASCII en el formato de archivo**
La opción de formato FBX7200ASCII se ha agregado en el programa FileFormat. Representa el formato de archivo ASCII FBX, con la versión 7.2.0. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

### **Se añade la opción de ahorro binario FBX7200en FileFormat**
La opción de formato FBX7200Binary se ha agregado en el programa FileFormat. Representa el formato de archivo Binary FBX, con la versión 7.2.0. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

### **Se añade la opción de ahorro FBX7300ASCII en el formato de archivo**
La opción de formato FBX7300ASCII se ha agregado en el programa FileFormat. Representa el formato de archivo ASCII FBX, con la versión 7.3.0. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

### **Se añade la opción de ahorro binario FBX7300en FileFormat**
La opción de formato FBX7300Binary se ha agregado en el programa FileFormat. Representa el formato de archivo Binary FBX, con la versión 7.3.0. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

### **La opción de guardado WavefrontOBJ se agrega en FileFormat y FileFormatType**
La opción de formato WavefrontOBJ se ha agregado en las enumeraciones FileFormat y FileFormatType. Representa el formato de archivo Obj Wavefront. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

