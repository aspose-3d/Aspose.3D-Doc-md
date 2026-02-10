---
title: 以球体半径工作
type: docs
weight: 50
url: /zh/java/working-with-radius-of-sphere/
description: 使用 Aspose.3D for Java，您可以设置球体的获取半径。
---
##  **以球体半径工作**
使用 Aspose.3D for Java，您可以设置球体的获取半径。为了获取或设置半径，您可以使用 `Sphere` 类的 `getRadius()` 和 `setRadius()` 方法。以下是设置球体半径的代码示例。

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
