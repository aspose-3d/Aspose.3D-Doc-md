---
title: 3D sahnesinde dikdörtgen torus oluştur
type: docs
weight: 50
url: /tr/net/create-rectangular-torus-in-3d-scene/
description: Aspose.3D for .NET API kullanarak, geliştiriciler 3D nesneleri oluşturabilir ve daha sonra herhangi bir desteklenen 3D formatında 3D sahneyi kaydedebilir.
---
{{% alert color="primary" %}} 

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, developers can create 3D objects, and then save 3D scene in any supported 3D format.

{{% /alert %}} 
##  **Angular ectangular Torus**
We have added `RectangularTorus` class, it allows developers to place a parameterized rectangular torus into the scene, this can be converted to ordinal mesh/triangle mesh during saving the scene into different supported file formats.

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

To dikdörtgen torus aşağıdaki gibi görünüyor:

! [Todo: image_alt_text](create-rectangular-torus-in-3d-scene_1.png)
