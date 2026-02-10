---
title: Lavorare con il raggio della sfera
type: docs
weight: 50
url: /it/java/working-with-radius-of-sphere/
description: Utilizzando Aspose.3D for Java, puoi impostare il raggio di ottenete di una sfera.
---
##  **Lavorare con il raggio della sfera**
Utilizzando Aspose.3D for Java, puoi impostare il raggio di utilizzo di una sfera. Per ottenere o impostare il raggio, puoi utilizzare i metodi `getRadius()` e `setRadius()` della classe `Sphere`. Di seguito è riportato il codice di esempio per impostare il raggio di una sfera.

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
