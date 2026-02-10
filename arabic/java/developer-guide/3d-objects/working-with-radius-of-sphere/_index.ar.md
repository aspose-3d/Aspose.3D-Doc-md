---
title: Working مع Radius من Sphere
type: docs
weight: 50
url: /ar/java/working-with-radius-of-sphere/
description: باستخدام Aspose.3D for Java ، يمكنك تعيين الحصول على نصف قطر كروي.
---
##  **Working مع Radius من Sphere**
باستخدام Aspose.3D for Java ، يمكنك ضبط الحصول على نصف قطر كروي. من أجل الحصول على نصف قطر أو ضبطه ، يمكنك استخدام طرق `getRadius()` و `setRadius()` لفئة `Sphere`. فيما يلي عينة الكود لتعيين نصف قطر كروي.

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
