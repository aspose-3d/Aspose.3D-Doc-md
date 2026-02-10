---
title: Работа с радиусом сферы
type: docs
weight: 50
url: /ru/java/working-with-radius-of-sphere/
description: Используя Aspose.3D for Java, можно задать радиус получения сферы.
---
##  **Работа с радиусом сферы**
Используя Aspose.3D for Java, можно задать радиус получения сферы. Чтобы получить или установить радиус, вы можете использовать методы `getRadius()` и `setRadius()` класса `Sphere`. Ниже приведен пример кода для установки радиуса сферы.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java

        // initialize a scene
        Scene scene = new Scene();
        // initialize a Sphere
        Sphere sphere = new Sphere();
        // set radius
        sphere.setRadius(10);
        // add sphere to the scene
        scene.getRootNode().createChildNode(sphere);
        // save scene
        scene.save("sphere.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}
