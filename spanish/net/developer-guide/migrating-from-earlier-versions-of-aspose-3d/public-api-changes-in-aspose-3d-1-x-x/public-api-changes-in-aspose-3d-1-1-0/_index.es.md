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
- [WavefrontOBJ Opción de ahorro se agrega en FileFormat y FileFormatType](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 1.0.0 to 1.1.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Se añade la opción de ahorro FBX7200ASCII en el formato de archivo**
La opción de formato FBX7200ASCII se ha agregado en el archivo FileFormat enum. Representa el formato de archivo ASCII FBX, con versión 7.2.0. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

###  **Se añade la opción de ahorro binario FBX7200en FileFormat**
La opción de formato binario FBX7200Binary se ha agregado en el archivo FileFormat enum. Representa el formato de archivo Binary FBX, con la versión 7.2.0. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

###  **Se añade la opción de ahorro FBX7300ASCII en el formato de archivo**
La opción de formato FBX7300ASCII se ha agregado en FileFormat enum. Representa el formato de archivo ASCII FBX, con versión 7.3.0. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

###  **Se añade la opción de ahorro binario FBX7300en FileFormat**
La opción de formato binario FBX7300Binary se ha agregado en FileFormat enum. Representa el formato de archivo Binary FBX, con la versión 7.3.0. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

###  **WavefrontOBJ Opción de ahorro se agrega en FileFormat y FileFormatType**
La opción de formato WavefrontOBJ se ha agregado en las enumeraciones FileFormat y FileFormatType. Representa el formato de archivo Obj de Wavefront. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

