---
title: Добавить информацию об активе в документ 3D
type: docs
weight: 10
url: /ru/java/add-asset-information-to-3d-document/
description: Метаданные-это структурированная информация, которая описывает, объясняет, находит или упрощает извлечение, использование или управление информационным ресурсом. Aspose.3D for Java API поддерживает определение метаданных для сцены.
---
##  **Добавить информацию об активе в документ 3D**
Метаданные-это структурированная информация, которая описывает, объясняет, находит или упрощает извлечение, использование или управление информационным ресурсом. Aspose.3D for Java API поддерживает определение метаданных для сцены.
###  **Определите метаданные для сцены**
3D показывает производство огромного количества метаданных и информации о изображениях. Метаданные-это актив и часть шоу.

1. Инициализируйте сцену 3D, используя класс `Scene`.
1. Установите имя приложения/инструмента.
1. Установите имя поставщика приложения/инструмента.
1. Установите единицу измерения.
1. Установите масштабный коэффициент единицы измерения.
1. Сохраните сцену 3D в поддерживаемом формате файла.

В этом примере мы предполагаем, что сцена создана инструментом CAD под названием «Египет», и она разработана «Manualdesk»:

{{< highlight "java" >}}
// Initialize a 3D scene
Scene scene = new Scene();
// Set application/tool name
scene.getAssetInfo().setApplicationName("Egypt");
// Set application/tool vendor name
scene.getAssetInfo().setApplicationVendor("Manualdesk");
// We use ancient egyption measurement unit Pole
scene.getAssetInfo().setUnitName("pole");
// One Pole equals to 60cm
scene.getAssetInfo().setUnitScaleFactor(0.6);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("InformationToScene.fbx");
// Save scene to 3D supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
