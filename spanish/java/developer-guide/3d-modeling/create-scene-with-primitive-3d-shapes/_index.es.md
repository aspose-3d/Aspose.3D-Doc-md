---
title: Crear escena con formas 3D primitivas
type: docs
weight: 20
url: /es/java/create-scene-with-primitive-3d-shapes/
description: Aspose.3D for Java API tiene soporte de formas primitivas 3D. Todas las primitivas parametrizadas se convertirán en malla automáticamente mientras se guardan en cualquier formato de archivo de salida compatible.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API tiene soporte de formas primitivas 3D. Todas las primitivas parametrizadas se convertirán en malla automáticamente mientras se guardan en cualquier formato de archivo de salida compatible.

{{% /alert %}} 
##  **Construir escena a partir de formas primitivas 3D**
El modelado es el proceso de creación pura y Aspose.3D API apoya la creación de una escena con formas primitivas 3D.
###  **Muestra de programación**
En este ejemplo de código se crea una escena con formas primitivas 3D y se guarda en el archivo FBX.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.getRootNode().createChildNode("box", new Box());
// Create a Cylinder model
scene.getRootNode().createChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
MyDir = MyDir + RunExamples.getOutputFilePath("test.fbx");
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
