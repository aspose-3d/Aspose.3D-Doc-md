---
title: Arbeta med sfärens radie
type: docs
weight: 50
url: /sv/java/working-with-radius-of-sphere/
description: Genom att använda Aspose.3D for Java kan du hämta radie av en sfär.
---
##  **Arbeta med sfärens radie**
Genom att använda Aspose.3D for Java kan du hämta radie av en sfär. För att få eller ställa in radie kan du använda `getRadius()` och `setRadius()`-metoder i klassen `Sphere`. Nedan följer kodprovet för att ställa in en sfärs radie.

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
