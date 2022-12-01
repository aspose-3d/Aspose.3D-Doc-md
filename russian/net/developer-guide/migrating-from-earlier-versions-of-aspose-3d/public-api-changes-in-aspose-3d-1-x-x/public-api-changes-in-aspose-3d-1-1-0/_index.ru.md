---
title: Публичные API Изменения в Aspose.3D 1.1.0
type: docs
weight: 60
url: /ru/net/public-api-changes-in-aspose-3d-1-1-0/
---
**Содержание Резюме**

- [Вариант сохранения FBX7200ASCII добавлен в FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [Вариант FBX7200Binary Saving добавлен в FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [Вариант сохранения FBX7300ASCII добавлен в FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [FBX7300Binary Saving Option добавлена в FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [WavefrontOBJ Вариант сохранения добавлен в FileFormat и FileFormatType](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API от версии 1.0.0 до 1.1.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
### **Вариант сохранения FBX7200ASCII добавлен в FileFormat**
Опция формата FBX7200ASCII была добавлена в FileFormat enum. Он представляет формат файла ASCII FBX с версией 7.2.0. Пример кода:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

### **Вариант FBX7200Binary Saving добавлен в FileFormat**
Опция формата FBX7200Binary была добавлена в FileFormat enum. Он представляет двоичный формат файла FBX с версией 7.2.0. Пример кода:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

### **Вариант сохранения FBX7300ASCII добавлен в FileFormat**
Опция формата FBX7300ASCII была добавлена в FileFormat enum. Он представляет формат файла ASCII FBX с версией 7.3.0. Пример кода:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

### **FBX7300Binary Saving Option добавлена в FileFormat**
Опция формата FBX7300Binary была добавлена в FileFormat enum. Он представляет двоичный формат файла FBX с версией 7.3.0. Пример кода:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

### **WavefrontOBJ Вариант сохранения добавлен в FileFormat и FileFormatType**
Опция формата WavefrontOBJ была добавлена в формате FileFormat и FileFormatType. Он представляет формат файла Obj Wavefront. Пример кода:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

