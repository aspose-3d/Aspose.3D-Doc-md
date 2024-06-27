---
title: Personalizar RotationOrder en el archivo FBX
type: docs
weight: 10
url: /es/net/customize-rotation-order-in-fbx-file
description: Usando Aspose.3D for .NET, los desarrolladores pueden definir personalizar las propiedades nativas FBX como RotationOrder.
---
{{% alert color="primary" %}}

Usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), a veces, los desarrolladores requieren un control preciso sobre las características específicas del formato, como cambiar el `RotationOrder` en el exportador FBX. Si bien es posible que no haya un API público que exponga directamente esta funcionalidad, Aspose.3D for .NET proporciona formas de lograr tales personalizaciones a través de su arquitectura flexible.
{{% /alert %}}



Así es como puedes manejar esto en Aspose.3D:

{{% highlight "csharp" %}}

var rvm = Scene.FromFile(@"F1234.rvm");
rvm.RootNode.Accept((Node node) =>
{
    node.SetProperty("RotationOrder", 1); //set a custom property, exporter will match this to FBX's property.
    return true; //continue to traverse on other nodes 
});

rvm.Save(@"test.fbx");

{{% /highlight %}}

En este ejemplo:

1. Cree una escena a partir de un archivo RVM.
1. Visita todos los nodos de la escena.
1. Establecer propiedad personalizada: el método SetProperty se utiliza para establecer la propiedad `RotationOrder`, demostrando cómo pueden aprovecharse los mecanismos internos para controlar las características específicas del formato no expuestas directamente por el API público.
1. Guardar la escena: La escena se guarda con el `RotationOrder` personalizado.

Mediante el uso de tales técnicas, Aspose.3D permite a los desarrolladores ajustar y controlar características específicas de los formatos 3D, asegurando que se cumplan requisitos detallados y precisos en varias aplicaciones 3D.