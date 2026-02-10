---
title: Arbeiten mit Radius of Sphere
type: docs
weight: 50
url: /de/java/working-with-radius-of-sphere/
description: Mit Aspose.3D for Java können Sie den Abhol radius einer Kugel festlegen.
---
##  **Arbeiten mit Radius of Sphere**
Mit Aspose.3D for Java können Sie den Abhol radius einer Kugel festlegen. Um Radius zu erhalten oder festzulegen, können Sie `getRadius()` und `setRadius()` Methoden der `Sphere` Klasse verwenden. Das Folgende ist das Code beispiel, um den Radius einer Kugel festzulegen.

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
