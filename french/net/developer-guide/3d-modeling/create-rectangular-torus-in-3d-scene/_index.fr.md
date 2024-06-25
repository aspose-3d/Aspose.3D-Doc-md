---
title: Créer un torus rectangulaire dans 3D Scène
type: docs
weight: 50
url: /fr/net/create-rectangular-torus-in-3d-scene/
description: En utilisant Aspose.3D for .NET API, les développeurs peuvent créer des objets 3D, puis enregistrer une scène 3D dans n'importe quel format 3D pris en charge.
---
{{% alert color="primary" %}} 

En utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, les développeurs peuvent créer des objets 3D, puis enregistrer une scène 3D dans n'importe quel format 3D pris en charge.

{{% /alert %}} 
##  **Tore rectangulaire**
Nous avons ajouté la classe `RectangularTorus`, elle permet aux développeurs de placer un tore rectangulaire paramétré dans la scène, ce qui peut être converti en maillage ordinal/maillage triangulaire lors de l'enregistrement de la scène dans différents formats de fichiers pris en charge.

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

Le tore rectangulaire généré ressemble à ce qui suit:

! [Tout le monde: image_alt_text](create-rectangular-torus-in-3d-scene_1.png)
