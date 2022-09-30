---
title: Skapa rektangulär Torus i 3D Scene
type: docs
weight: 50
url: /sv/net/create-rectangular-torus-in-3d-scene/
description: Med Aspose.3D for .NET API kan utvecklare skapa 3D objekt, och sedan spara 3D scen i någon som stöds 3D format.
---
{{% alert color="primary" %}} 

Användning[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API, utvecklare kan skapa 3D objekt, och sedan spara 3D scen i någon som stöds 3D format.

{{% /alert %}} 
## **Rektangulär torus**
Vi har lagt till `RectangularTorus` klass, det tillåter utvecklare att placera en parameteriserad rektangulär torus i scenen, Detta kan konverteras till ordinarie mesh/triangelt mesh under att spara scenen till olika filformat som stöds.

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

Den genererade rektangulära torus ser ut enligt följande:

![TOD:imageName_Av_Text:](create-rectangular-torus-in-3d-scene_1.png)
