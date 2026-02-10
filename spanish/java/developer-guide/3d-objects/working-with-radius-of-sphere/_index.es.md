---
title: Trabajando con Radio de Esfera
type: docs
weight: 50
url: /es/java/working-with-radius-of-sphere/
description: Usando Aspose.3D for Java, puede establecer el radio de obtener de una esfera.
---
##  **Trabajando con Radio de Esfera**
Usando Aspose.3D for Java, puede establecer el radio de obtener de una esfera. Para obtener o establecer el radio, puede usar los métodos `getRadius()` y `setRadius()` de la clase `Sphere`. El siguiente es el ejemplo de código para establecer el radio de una esfera.

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
