---
title: Создать пустой документ 3D
type: docs
weight: 20
url: /ru/java/create-an-empty-3d-document/
description: Aspose.3D for Java API поддерживает создание сцены 3D с нуля, а затем сохранение в поддерживаемом формате 3D.
---
##  **Создайте пустую сцену 3D и сохраните ее в поддерживаемом формате 3D**
Aspose.3D for Java API поддерживает создание сцены 3D с нуля, а затем сохранение в поддерживаемом формате 3D.
###  **Создание пустой сцены 3D**
Пожалуйста, выполните следующие действия, чтобы создать сцену 3D с Aspose.3D for Java API:

1. Создать экземпляр**Сцена**Класс, представляющий сцену 3D.
1. Создать документ 3D, вызвав**Экономить**Метод**Сцена**Экземпляр класса.
####  **Создание пустой сцены 3D: образцы программирования**
{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "document.fbx";
// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}




