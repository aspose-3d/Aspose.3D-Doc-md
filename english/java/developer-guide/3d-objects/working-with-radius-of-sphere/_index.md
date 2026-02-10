---
title: Working with Radius of Sphere
type: docs
weight: 50
url: /java/working-with-radius-of-sphere/
description: Using Aspose.3D for Java, you can set of get radius of a sphere.
---

## **Working with Radius of Sphere**
Using Aspose.3D for Java, you can set of get radius of a sphere. In order to get or set radius, you can use `getRadius()` and `setRadius()` methods of `Sphere` class. The following is the code sample to set radius of a sphere.  

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
