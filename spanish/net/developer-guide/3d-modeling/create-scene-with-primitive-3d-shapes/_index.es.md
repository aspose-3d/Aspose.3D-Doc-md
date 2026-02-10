---
title: Crear escena con formas 3D primitivas
type: docs
weight: 10
url: /es/net/create-scene-with-primitive-3d-shapes/
description: Usando Aspose.3D for .NET, los desarrolladores pueden definir una escena con formas 3D primitivas. Todas las primitivas parametrizadas se convertirán en malla automáticamente mientras se guardan en cualquier formato de archivo de salida compatible.
---
{{% alert color="primary" %}}

Usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), los desarrolladores pueden definir una escena con formas 3D primitivas. Todas las primitivas parametrizadas se convertirán en malla automáticamente mientras se guardan en cualquier formato de archivo de salida compatible.

{{% /alert %}}
##  **Construir escena a partir de formas primitivas 3D**
El modelado es el proceso de creación pura y Aspose.3D API apoya la creación de una escena con formas primitivas 3D.
###  **Muestra de programación**
En este ejemplo de código se crea una escena con formas primitivas 3D y se guarda en el archivo FBX.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.RootNode.CreateChildNode("box", new Box());
// Create a Cylinder model
scene.RootNode.CreateChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
scene.Save("test.fbx");


{{< /highlight >}}
