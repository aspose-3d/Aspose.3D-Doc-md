---
title: Добавление преобразования к узлу
type: docs
weight: 10
url: "/ru/nodejs-java/adding-transformation-to-the-node/"
description: "Aspose.3D для Node.js через Java API поддерживает поворот объектов в 3D пространстве. Существует три способа определения поворота объекта в 3D пространстве: углы Эйлера, кватернионы и пользовательская матрица, все они поддерживаются классом Transform."
---

{{% alert color="primary" %}}

Aspose.3D для Node.js через Java API имеет поддержку вращения объектов в 3D пространстве. Существуют три способа определения вращения объекта в 3D пространстве: углы Эйлера, кватернионы и пользовательская матрица, все они поддерживаются классом `Transform`.

{{% /alert %}}

TSR (Translation/Scaling/Rotation) наиболее часто используются в 3D сценариях, мы предоставили класс `Transform` для доступа к этим в Aspose.3D. Аффинные преобразования включают:

- Translation (Перенос)
- Scaling (Масштабирование)
- Rotation (Вращение)
- Shear mapping (Сдвиг)
- Squeeze mapping (Сжатие)

## **Вращение с помощью углов Эйлера**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Инициализация объекта сцены
var scene = new aspose.threed.Scene();

// Инициализация цилиндра
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Создание ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Углы Эйлера
Node.getTransform().setEulerAngles(new aspose.threed.Vector3(30, 40, 50));

// Установка переноса
Node.getTransform().setTranslation(new aspose.threed.Vector3(0, 0, 20));

// Сохранение
scene.save("TransformationToNode.obj");

{{< /highlight >}}

## **Пользовательская матрица преобразования**
Мы также можем использовать Matrix напрямую:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Инициализация объекта сцены
var scene = new aspose.threed.Scene();

// Инициализация цилиндра
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Создание ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Установка пользовательской матрицы переноса
Node.getTransform().setTransformMatrix(new aspose.threed.Matrix4(
    1, -0.3, 0, 0,
    0.4, 1, 0.3, 0,
    0, 0, 1, 0,
    0, 20, 0, 1
));

// Сохранение
scene.save("TransformationToNode.obj");

{{< /highlight >}}
