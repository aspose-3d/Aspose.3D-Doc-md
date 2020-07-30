---
title : "Create rectangular Torus in 3D Scene" 
description : "" 
weight : 12043 
toc : false
type: docs
url: /net/developerguide/3dobjects/create+rectangular+torus+in+3d+scene/
---

# Aspose.3D for .NET : Create rectangular Torus in 3D Scene


Using [Aspose.3D for .NET](https://products.aspose.com/3d/net) API, developers can create 3D objects, and then save 3D scene in any supported 3D format.

## Rectangular Torus

We have added `RectangularTorus` class, it allows developers to place a parameterized rectangular torus into the scene, this can be converted to ordinal mesh/triangle mesh during saving the scene into different supported file formats.

**C#**

{{< code lang="c#" >}}
RectangularTorus rt = new RectangularTorus();
rt.InnerRadius = 17;
rt.OuterRadius = 22;
rt.Height = 30;
rt.Arc = Math.PI * 0.5;
Scene scene = new Scene();
scene.RootNode.CreateChildNode(rt);
scene.Save("rtorus.obj", FileFormat.WavefrontOBJ);
{{< /code >}}

The generated rectangular torus looks as follows:

![](https://docs2.aspose.com/3d/net/attachments/61539825/61767722.png)

## Attachments:

![](https://docs2.aspose.com/3d/net/images/icons/bullet_blue.gif) [rtorus.png](https://docs2.aspose.com/3d/net/attachments/61539825/61767722.png) (image/png)  

