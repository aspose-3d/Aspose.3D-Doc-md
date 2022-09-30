---
title: Публичные API Изменения в Aspose.3D 17.2.0
type: docs
weight: 10
url: /ru/net/public-api-changes-in-aspose-3d-17-2-0/
---
**Содержание Резюме**

- [Импорт файлов DirectX X](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [Добавляет класс Aspose.ThreeD.Formats.X.XLoadOptions](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API с версии 17.1.0 до 17.2.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
#### **Импорт файлов DirectX X**
Используя последнюю версию (17,02) или выше, разработчики могут импортировать файлы X. Записи формата XBinary и XText добавляются для импорта двоичных файлов и файлов ASCII X.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
#### **Добавляет класс Aspose.ThreeD.Formats.X.XLoadOptions**
Мы добавили класс XLoadOptions. Он помогает импортировать файлы X в Aspose.3D API.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// initialize Scene class object

Scene scene = new Scene();

// initialize an object

XLoadOptions loadXOpts = new XLoadOptions();

// load X file

scene.Open( "3DX.x", loadXOpts);

{{< /highlight >}}
