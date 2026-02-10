---
title: Кодирование сетки 3D в файле Google Draco
type: docs
weight: 30
url: /ru/java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Java API поддерживает импорт модели 3D, получение сетки, а затем кодирование сетки в файле Google Draco.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API поддерживает импорт модели 3D, получение сетки, а затем кодирование сетки в файле Google Draco. Разработчики также могут указать положение, координаты текстуры, цвет и нормальные биты, а также уровень сжатия перед кодированием сетки.

{{% /alert %}} 
##  **Получить 3D Mesh и закодировать в Google Draco файле**
Метод кодирования, представленный классом `DracoFormat`, можно использовать для кодирования сетки 3D в файле Google Draco. В качестве параметров используются объекты `Mesh` и `DracoSaveOptions`. С параметрами сохранения Draco разработчики также могут указать положение, координаты текстуры, цвет и нормальные биты, а также уровень сжатия перед кодированием сетки.
###  **Образец программирования**
Этот пример кода извлекает Mesh of Sphere, а затем кодируют в файле Google Draco после указания уровня сжатия.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Create a sphere
Sphere sphere = new Sphere();
// Encode the sphere to Google Draco raw data using optimal compression level.
DracoSaveOptions opt = new DracoSaveOptions();
opt.setCompressionLevel(DracoCompressionLevel.OPTIMAL);
byte[] b = FileFormat.DRACO.encode(sphere.toMesh(), opt);
// Save the raw bytes to file
Files.write(Paths.get(MyDir, "SphereMeshtoDRC_Out.drc"), b);
{{< /highlight >}}
