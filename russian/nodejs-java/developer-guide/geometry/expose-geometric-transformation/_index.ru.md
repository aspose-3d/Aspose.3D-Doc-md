---
title: Предоставить геометрическое преобразование
type: docs
weight: 50
url: "/ru/nodejs-java/expose-geometric-transformation/"
description: "Aspose.3D для Node.js через Java позволяет выводить геометрическое преобразование 3D-сцены. Вы можете вычислить глобальное преобразование, используя метод evaluateGlobalTransform."
---

# **Отображение геометрического преобразования**
Aspose.3D для Node.js через Java позволяет отображать геометрическое преобразование 3D-сцены. Вы можете вычислить глобальное преобразование с помощью метода `evaluateGlobalTransform`. Следующий фрагмент кода показывает, как отобразить геометрическое преобразование.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Инициализация объекта сцены
var scene = new aspose.threed.Scene();

// Инициализация цилиндра
var cylinder =new aspose.threed.Cylinder();

// Создание ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Получение геометрического перемещения
Node.getTransform().setGeometricTranslation(new aspose.threed.Vector3(10, 0, 0));

// Первый Console.WriteLine выведет матрицу преобразования, включающую геометрическое преобразование
// в то время как второй не выведет.
console.log(Node.evaluateGlobalTransform(true));
console.log(Node.evaluateGlobalTransform(false));

{{< /highlight >}}