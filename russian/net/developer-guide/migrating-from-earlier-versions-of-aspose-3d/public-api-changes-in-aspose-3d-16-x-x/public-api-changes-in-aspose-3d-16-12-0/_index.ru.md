---
title: Публичные API Изменения в Aspose.3D 16.12.0
type: docs
weight: 10
url: /ru/net/public-api-changes-in-aspose-3d-16-12-0/
---
**Содержание Резюме**

- [Добавляет Aspose.ThreeD. Класс с дозированным](#PublicAPIChangesinAspose.3D16.12.0-AddsAspose.ThreeD.MeteredClass)
- [Импорт файлов DXF](#PublicAPIChangesinAspose.3D16.12.0-ImportingDXFFiles)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API с версии 16.11.0 до 16.12.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
### **Добавляет Aspose.ThreeD. Класс с дозированным**
Способ применения дипломированных лицензий.

**C#**

{{< highlight "java" >}}

 // initialize a metered license class object

Metered metered = new Metered();

// set public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

//Your other code to use Aspose.3D

{{< /highlight >}}
### **Импорт файлов DXF**
Используя последнюю версию (16.12.0) или выше, разработчики могут импортировать файлы DXF. Запись формата DXF добавлена для целей загрузки.

**C#**

{{< highlight "java" >}}

 // an entry of DXF file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat DXF;

// load a DXF file

Scene dxfFile = new Scene("wuson.dxf");

{{< /highlight >}}
