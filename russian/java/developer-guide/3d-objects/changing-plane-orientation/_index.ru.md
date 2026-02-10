---
title: Изменение ориентации плоскости
type: docs
weight: 70
url: /ru/java/changing-plane-orientation/
description: Aspose.3D for Java позволяет изменять ориентацию сцены. Для того чтобы изменить ориентацию, методы getUp() и setUp() вводятся в класс плоскости.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,5 или выше.

{{% /alert %}} 
#  **Изменение ориентации плоскости**
Aspose.3D for Java позволяет изменять ориентацию сцены. Чтобы изменить ориентацию, в классе `Plane` введены методы `getUp()` и `setUp()`. Следующий фрагмент кода показывает, как изменить ориентацию самолета:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize Scene
Scene scene = new Scene();
// Initialize Plane
Plane plane = new Plane();
// Set Vector
plane.setUp(new Vector3(1, 1, 3));
scene.getRootNode().createChildNode(plane);
//This will generate a plane that has customized orientation
scene.save(MyDir+"ChangePlaneOrientation.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}
