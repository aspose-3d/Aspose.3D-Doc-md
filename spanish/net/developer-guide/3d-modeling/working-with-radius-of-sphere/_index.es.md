---
title: Trabajando con Radio de Esfera
type: docs
weight: 110
url: /es/net/working-with-radius-of-sphere/
description: Usando Aspose.3D for .NET, puede establecer el radio de obtener de una esfera. Para obtener o establecer el radio, puede usar la propiedad Radius de la clase Sphere. El siguiente es el ejemplo de código para establecer el radio de una esfera.
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,4 o superior.

{{% /alert %}} 
##  **Trabajar con Radio de la Esfera**
Usando Aspose.3D for .NET, puede establecer el radio de obtener de una esfera. Para obtener o establecer el radio, puede usar la propiedad `Radius` de la clase `Sphere`. El siguiente es el ejemplo de código para establecer el radio de una esfera.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a Scene
Scene scene = new Scene();
// Set Sphere Radius (Using Radius property you can get or set radius of Sphere)
scene.RootNode.CreateChildNode(new Sphere() { Radius = 10 });
// Save scene
scene.Save("sphere.obj");

{{< /highlight >}}
