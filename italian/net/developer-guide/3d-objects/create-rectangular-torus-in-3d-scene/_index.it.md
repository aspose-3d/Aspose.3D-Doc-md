---
title: Creare Torus rettangolare nella scena 3D
type: docs
weight: 50
url: /it/net/create-rectangular-torus-in-3d-scene/
description: Utilizzando Aspose.3D for .NET API, gli sviluppatori possono creare oggetti 3D e quindi salvare la scena 3D in qualsiasi formato 3D supportato.
---
{{% alert color="primary" %}} 

Utilizzo[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API, gli sviluppatori possono creare 3D oggetti e quindi salvare la scena 3D in qualsiasi formato 3D supportato.

{{% /alert %}} 
## **Torus rettangolare**
Abbiamo aggiunto la classe `RectangularTorus`, consente agli sviluppatori di inserire un toro rettangolare parametrizzato nella scena, questo può essere convertito in mesh/mesh triangolo ordinale durante il salvataggio della scena in diversi formati di file supportati.

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

Il toro rettangolare generato ha il seguente aspetto:

![Todo: immagine_Alt_Testo](create-rectangular-torus-in-3d-scene_1.png)
