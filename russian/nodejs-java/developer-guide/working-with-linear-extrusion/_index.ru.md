---
title: Работа с линейной экструзией
type: docs
weight: 80
url: "/ru/nodejs-java/working-with-linear-extrusion/"
description: "Aspose.3D для Node.js через Java предлагает класс LinearExtrusion, который принимает 2D-фигуру в качестве входных данных и расширяет фигуру в 3-м измерении."
---

# **Выполнение линейной экструзии**
Aspose.3D для Node.js через Java предлагает класс `LinearExtrusion`, который принимает 2D-фигуру в качестве входных данных и расширяет фигуру в 3-м измерении. Следующий фрагмент кода показывает, как выполнить линейную экструзию:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Инициализируйте базовую форму для экструзии
// Инициализируйте базовый профиль для экструзии
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Выполните линейную экструзию, передав 2D-фигуру в качестве входных данных и расширив фигуру в 3-м измерении
var extrusion =new aspose.threed.LinearExtrusion(profile, 10);
extrusion.setSlices(100);
extrusion.setCenter(true);
extrusion.setTwist(360);
extrusion.setTwistOffset(new aspose.threed.Vector3(10, 0, 0));

// Создайте сцену
var scene = new aspose.threed.Scene();

// Создайте дочерний узел, передав экструзию
scene.getRootNode().createChildNode(extrusion);

// Сохраните 3D-сцену
scene.save("LinearExtrusion.obj");

{{< /highlight >}}

# **Слайсы в линейной экструзии**
Aspose.3D для Node.js через Java предлагает метод `setSlices()` класса `LinearExtrusion`. Метод `setSlices()` определяет количество промежуточных точек вдоль пути экструзии. Следующий фрагмент кода показывает, как использовать метод `setSlices()` в линейной экструзии:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Инициализируйте базовый профиль для экструзии
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Создайте сцену
var scene = new aspose.threed.Scene();

// Создайте левый узел
var left=scene.getRootNode().createChildNode();
// Создайте правый узел
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Параметр Slices определяет количество промежуточных точек вдоль пути экструзии
// Выполните линейную экструзию на левом узле, используя свойство slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(2);
left.createChildNode(extrusion1);

// Выполните линейную экструзию на правом узле, используя свойство slices
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(10);
right.createChildNode(extrusion2);

// Сохраните 3D-сцену
scene.save("SlicesInLinearExtrusion.obj");

{{< /highlight >}}

# **Центр в линейной экструзии**
Aspose.3D для Node.js через Java предлагает метод `setCenter()` класса `LinearExtrusion`. Если метод `setCenter()` установлен в значение true, диапазон экструзии составляет от -Height/2 до Height/2, в противном случае экструзия происходит от 0 до Height. Следующий фрагмент кода показывает, как использовать метод `setCenter()` в линейной экструзии:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Инициализируйте базовый профиль для экструзии
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Создайте сцену
var scene = new aspose.threed.Scene();

// Создайте левый узел
var left=scene.getRootNode().createChildNode();
// Создайте правый узел
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Установите плоскость основания для справки
var box=new aspose.threed.Box(0.01, 3, 3);

// Если свойство Center имеет значение true, диапазон экструзии составляет от -Height/2 до Height/2, в противном случае экструзия происходит от 0 до Height
// Выполните линейную экструзию на левом узле, используя свойства center и slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(3);
extrusion1.setCenter(false);
left.createChildNode(extrusion1);
left.createChildNode(box);

// Выполните линейную экструзию на правом узле, используя свойства center и slices
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(3);
extrusion2.setCenter(true);
right.createChildNode(extrusion2);
right.createChildNode(box);

// Сохраните 3D-сцену
scene.save("CenterInLinearExtrusion.obj");

{{< /highlight >}}

# **Поворот в линейной экструзии**
Aspose.3D для Node.js через Java предлагает метод `setTwist()` класса `LinearExtrusion`. Метод `setTwist()` обрабатывает степень вращения при экструзии фигуры. Следующий фрагмент кода показывает, как использовать метод `setTwist()` в линейной экструзии:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Инициализируйте базовый профиль для экструзии
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Создайте сцену
var scene = new aspose.threed.Scene();

// Создайте левый узел
var left=scene.getRootNode().createChildNode();
// Создайте правый узел
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Свойство Direction определяет направление экструзии.
// Выполните линейную экструзию на левом узле, используя свойства twist и slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Выполните линейную экструзию на правом узле, используя свойства twist, twist offset и slices
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setTwistOffset(new aspose.threed.Vector3(3, 0, 0));
right.createChildNode(extrusion2);

// Сохраните 3D-сцену
scene.save("TwistOffsetInLinearExtrusion.obj");

{{< /highlight >}}

# **Направление в линейной экструзии**
Aspose.3D для Node.js через Java предлагает метод `setDirection()` класса `LinearExtrusion`. Метод `setDirection()` определяет направление экструзии. Следующий фрагмент кода показывает, как использовать метод `setDirection()` в линейной экструзии:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Инициализируйте базовый профиль для экструзии
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Создайте сцену
var scene = new aspose.threed.Scene();

// Создайте левый узел
var left=scene.getRootNode().createChildNode();
// Создайте правый узел
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Свойство Direction определяет направление экструзии.
// Выполните линейную экструзию на левом узле, используя свойства twist и slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Выполните линейную экструзию на правом узле, используя свойства twist, slices и direction
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setDirection(new aspose.threed.Vector3(0.3, 0.2, 1));
right.createChildNode(extrusion2);

// Сохраните 3D-сцену
scene.save("DirectionInLinearExtrusion.obj");


{{< /highlight >}}