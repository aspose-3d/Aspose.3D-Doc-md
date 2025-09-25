---
title: Создать сцену с примитивными 3D формами
type: docs
weight: 20
url: "/ru/nodejs-java/create-scene-with-primitive-3d-shapes/"
description: "Aspose.3D для Node.js через Java API поддерживает примитивные 3D-фигуры. Все параметризованные примитивы будут автоматически преобразованы в сетку при сохранении в любой поддерживаемый формат выходного файла."
---

{{% alert color="primary" %}} 

Aspose.3D для Node.js через Java API имеет поддержку примитивных 3D-фигур. Все параметризованные примитивы будут автоматически преобразованы в сетку при сохранении в любом поддерживаемом формате выходного файла.

{{% /alert %}} 
## **Создание сцены из примитивных 3D-фигур**
Моделирование — это процесс чистого творчества, и API Aspose.3D поддерживает создание сцены с примитивными 3D-фигурами.
### **Пример программирования**
Этот пример кода создает сцену с примитивными 3D-фигурами и сохраняет ее в файле OBJ.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Инициализация 3D-сцены
var scene = new aspose.threed.Scene();

// Создание модели Box
scene.getRootNode().createChildNode("box", new aspose.threed.Box());

// Создание модели Cylinder
scene.getRootNode().createChildNode("cylinder", new aspose.threed.Cylinder());

// Сохранение чертежа в формате OBJ
scene.save("test.obj");


{{< /highlight >}}