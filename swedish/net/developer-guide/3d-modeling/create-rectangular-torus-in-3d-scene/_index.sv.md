---
title: Skapa rektangulärt torus i 3D Scene
type: docs
weight: 50
url: /sv/net/create-rectangular-torus-in-3d-scene/
description: Använder Aspose. 3D for .NET API, utvecklare kan skapa 3D objekt, och sedan spara 3D scen i vilket 3D-format som stöds.
---
{{% alert color="primary" %}} 

Genom att använda [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, kan utvecklare skapa 3D objekt, och sedan spara 3D scen i vilket 3D-format som stöds.

{{% /alert %}} 
##  **Rektangulär torus**
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

![todo:image_alt_text](create-rectangular-torus-in-3d-scene_1.png)
