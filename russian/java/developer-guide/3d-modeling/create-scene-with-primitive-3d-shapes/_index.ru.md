---
title: Создайте сцену с примитивными формами 3D
type: docs
weight: 20
url: /ru/java/create-scene-with-primitive-3d-shapes/
description: Aspose.3D for Java API поддерживает примитивные формы 3D. Все параметризованные примитивы будут автоматически преобразованы в mesh при сохранении в любом поддерживаемом формате выходного файла.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API поддерживает примитивные формы 3D. Все параметризованные примитивы будут автоматически преобразованы в mesh при сохранении в любом поддерживаемом формате выходного файла.

{{% /alert %}} 
##  **Построить сцену из примитивных 3D фигур**
Моделирование-это процесс чистого создания и Aspose.3D API поддерживает создание сцены с примитивными 3D формами.
###  **Образец программирования**
В этом примере кода создается сцена с примитивными фигурами 3D и сохраняется в файле FBX.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.getRootNode().createChildNode("box", new Box());
// Create a Cylinder model
scene.getRootNode().createChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
MyDir = MyDir + RunExamples.getOutputFilePath("test.fbx");
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
