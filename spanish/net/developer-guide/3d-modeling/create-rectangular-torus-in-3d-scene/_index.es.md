---
title: Crear un toro rectangular en la escena 3D
type: docs
weight: 50
url: /es/net/create-rectangular-torus-in-3d-scene/
description: Con Aspose.3D for .NET API, los desarrolladores pueden crear objetos 3D y luego guardar la escena 3D en cualquier formato 3D compatible.
---
{{% alert color="primary" %}} 

Usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, los desarrolladores pueden crear objetos 3D y luego guardar la escena 3D en cualquier formato 3D compatible.

{{% /alert %}} 
##  **Torus rectangular**
Hemos agregado la clase `RectangularTorus`, permite a los desarrolladores colocar un toro rectangular parametrizado en la escena, esto se puede convertir en malla ordinal/malla triangular durante el guardado de la escena en diferentes formatos de archivo compatibles.

**C#**

{{< highlight "java" >}}

 RectangularTorus rt = new RectangularTorus();

rt.InnerRadius = 17;

rt.OuterRadius = 22;

rt.Height = 30;

rt.Arc = Math.PI * 0.5;

Scene scene = new Scene();

scene.RootNode.CreateChildNode(rt);

scene.Save("rtorus.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

El toro rectangular generado se ve de la siguiente manera:

¡! [Todo: image_alt_text](create-rectangular-torus-in-3d-scene_1.png)
