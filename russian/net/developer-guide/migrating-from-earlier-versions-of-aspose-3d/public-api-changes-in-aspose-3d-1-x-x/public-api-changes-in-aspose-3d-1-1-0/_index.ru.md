---
title: Публичные изменения API в Aspose.3D 1.1.0
type: docs
weight: 60
url: /ru/net/public-api-changes-in-aspose-3d-1-1-0/
---
**Содержание Резюме**

- [Вариант сохранения FBX7200ASCII добавлен в FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [Вариант FBX7200Binary Saving добавлен в FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [Вариант сохранения FBX7300ASCII добавлен в FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [FBX7300Binary Saving Option добавлена в FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [WavefrontOBJ Опция сохранения добавлена в FileFormat и FileFormatType](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API с версии 1.0.0 до 1.1.0, которые могут представлять интерес для разработчиков модулей/приложений. Она включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
###  **Вариант сохранения FBX7200ASCII добавлен в FileFormat**
Параметр формата FBX7200ASCII был добавлен в enum FileFormat. Он представляет формат файла ASCII FBX, с версией 7.2.0. Пример кода:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

###  **Вариант FBX7200Binary Saving добавлен в FileFormat**
В перечисление FileFormat добавлена опция формата FBX7200Binary. Он представляет собой формат файла Binary FBX с версией 7.2.0. Пример кода:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

###  **Вариант сохранения FBX7300ASCII добавлен в FileFormat**
В enum FileFormat добавлена опция формата FBX7300ASCII. Он представляет формат файла ASCII FBX, с версией 7.3.0. Пример кода:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

###  **FBX7300Binary Saving Option добавлена в FileFormat**
В enum FileFormat добавлена опция формата FBX7300Binary. Он представляет собой формат файла Binary FBX с версией 7.3.0. Пример кода:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

###  **WavefrontOBJ Опция сохранения добавлена в FileFormat и FileFormatType**
Параметр формата WavefrontOBJ был добавлен в enums FileFormat и FileFormatType. Он представляет формат файла Obj Wavefront. Пример кода:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

