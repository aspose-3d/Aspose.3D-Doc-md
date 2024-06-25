---
title: Публичные изменения API в Aspose.3D 16.9.0
type: docs
weight: 30
url: /ru/net/public-api-changes-in-aspose-3d-16-9-0/
---
**Содержание Резюме**

- [Импорт сцены 3D из источника PDF](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
  - [Adds Aspose.ThreeD.Formats.PdfLoadOptions Class](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)
  - [Adds Aspose.ThreeD.FileFormat and Aspose.ThreeD.Formats.PdfFormat Class](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)
- [Сохраните сцену 3D в формате PDF](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
  - [Adds Aspose.ThreeD.Formats.PdfSaveOptions class and Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode Enums](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)
- [Добавляет метод триангуляции в класс Aspose.ThreeD. Сущности. PolygonModifier](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Добавляет два метода BuildTangentBinormal в класс Aspose.ThreeD. Entity. PolygonModifier](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API с версии 2.1.0 до 16.9.0, которые могут представлять интерес для разработчиков модулей/приложений. Она включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
###  **Импорт сцены 3D из источника PDF**
Используя последнюю версию (16.9.0) или выше, разработчики могут получать сцены 3D из входного файла PDF.
####  **Добавляет Aspose.ThreeD. Форматы. Класс PdfLoadOptions**
Мы добавили класс PdfLoadOptions. Это помогает при загрузке содержимого из входного файла PDF. Разработчики могут применять пароль для защищенных PDF-файлов.

**Открыть сцену из защищенного паролем файла PDF**

{{< highlight "java" >}}

 // set path with filename and extension 

string path = @"House_Design.pdf";

// create a new scene

Scene scene = new Scene();

// use loading options and apply password

PdfLoadOptions opt = new PdfLoadOptions() {Password = Encoding.UTF8.GetBytes("password")};

// open scene

scene.Open(path, opt);

{{< /highlight >}}
####  **Добавляет Aspose.ThreeD.FileFormat и Aspose.ThreeD. Форматы. Класс PDFFormat**
Мы добавили запись формата PDF в класс FileFormat для загрузки и сохранения. Класс PdfFormat помогает манипулировать PDF-файлами.

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**Извлеките все необработанное содержимое 3D из файла PDF**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[] password = null;

// extract 3D contents

List<byte[]> contents = FileFormat.PDF.Extract(path, password);

int i = 1;

// iterate through the contents and in separate 3D files

foreach (byte[] content in contents)

{

    string fileName = "3d-" + (i++);

    File.WriteAllBytes(fileName, content);

}

{{< /highlight >}}

**Извлеките все сцены 3D и сохраните их в файл FBX**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[] password = null;

List<Scene> scenes = FileFormat.PDF.ExtractScene(path, password);

int i = 1;

// iterate through the scenes and save in 3D files

foreach (Scene scene in scenes)

{

    string fileName = "3d-" + (i++) + ".fbx";

    scene.Save(fileName, FileFormat.FBX7400ASCII);

}

{{< /highlight >}}
###  **Сохраните сцену 3D в формате PDF**
Используя последнюю версию (16.9.0) или выше, разработчики могут сохранять все поддерживаемые файлы 3D в формате PDF.
####  **Добавляет Aspose.ThreeD. Форматы. Класс PdfSaveOptions и Aspose.ThreeD. Форматы. Схема PDFLightingScheme/PdfRenderMode Сводки**
PdfSaveOptions помогает применить настройку перед сохранением в формате вывода PDF. Разработчики могут установить режим рендеринга и схему освещения перед сохранением сцены 3D в формате PDF, как показано ниже:

**Создайте 3D PDF с цилиндром и отрисовайте в режиме затененной иллюстрации с оптимизированным освещением CAD**

{{< highlight "java" >}}

 // create a new scene

Scene scene = new Scene();

// create a cylinder child node

scene.RootNode.CreateChildNode("cylinder", new Cylinder()).Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.DarkCyan)};

// set rendering mode and lighting scheme

PdfSaveOptions opt = new PdfSaveOptions();

opt.LightingScheme = PdfLightingScheme.CAD;

opt.RenderMode = PdfRenderMode.ShadedIllustration;

// save in the PDF format

scene.Save("output.pdf", opt);

{{< /highlight >}}
###  **Добавляет метод триангуляции в класс Aspose.ThreeD. Сущности. PolygonModifier**
Мы добавили еще одну перегрузку метода Triangulate в класс PolygonModifier, который принимает объект класса Scene в качестве параметра.

**Преобразовать все многоугольники в треугольники в файле FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
###  **Добавляет два метода BuildTangentBinormal в класс Aspose.ThreeD. Entity. PolygonModifier**
Мы добавили два метода BuildTangentBinormal в класс PolygonModifier. Один метод принимает объект класса Scene в качестве параметра, а другой-объект класса Mesh в качестве параметра.

**Построение касательных и бинонормальных данных для всех ячеек в файле FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
