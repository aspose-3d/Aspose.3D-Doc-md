---
title: Travailler avec le rayon de la sphère
type: docs
weight: 50
url: /fr/java/working-with-radius-of-sphere/
description: En utilisant Aspose.3D for Java, vous pouvez définir le rayon de get d'une sphère.
---
##  **Travailler avec le rayon de la sphère**
En utilisant Aspose.3D for Java, vous pouvez définir le rayon de get d'une sphère. Pour obtenir ou définir un rayon, vous pouvez utiliser les méthodes `getRadius()` et `setRadius()` de la classe `Sphere`. Voici l'exemple de code pour définir le rayon d'une sphère.

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
