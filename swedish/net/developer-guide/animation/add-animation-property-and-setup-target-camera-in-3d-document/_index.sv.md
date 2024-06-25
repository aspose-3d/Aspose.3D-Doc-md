---
title: Lägg till animeringsegenskaper och inställningskamera i dokumentet 3D.
type: docs
weight: 10
url: /sv/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: I Aspose.3D är objektanimation faktiskt nyckelram- animation som animerar på egenskaper. För att animera egenskaper behöver du en CurveMapping instans som kartlägger komponenter i en egenskap till olika kurvor, till exempel, en Vector3-egenskap kan ha 3 komponenter X/Y/Z, som kommer att ställa upp tre kanaler i CurveMapping, Varje kanal kan ha en uppsättning av kurvor.
---
##  **Add Animation property in 3D document**
Aspose.3D for .NET stöder att visa animerad scen. Den här artikeln förklarar förutsättningarna för att flytta ett föremål.
###  **Flytta kubens position**
{{% alert color="primary" %}}

Klassobjektet [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) används i koden. Vi kan [Skapa ett Mesh-klassobjekt som berättat där.](/3d/sv/net/create-and-read-an-existing-3d-scene/) och det måste animera den lokala översättningsegenskapen för noden också: [Lägga till omvandlingen i noden](/3d/sv/net/adding-transformation-to-the-node/).

{{% /alert %}}

I Aspose.3D är objektanimation faktiskt nyckelram- animation som animerar på egenskaper. För att animera egenskaper behöver du en `CurveMapping` instans som kartlägger komponenter i en egenskap till olika kurvor, t.ex. en `Vector3` egenskap kan ha 3 komponenter `X`/`Y`/`Z`, som kommer att ställa in tre kanaler i `CurveMapping`, varje kanal kan ha en uppsättning `Curve`.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-PropertyToDocument-AddAnimationPropertyToDocument.cs" >}}
##  **Ställ in målkameran i 3D fil**
Aspose.3D for .NET erbjuder att ställa in målkameran i 3D-fil. I vissa filformat, stöder ljus/kamera mål, vilket tillåter ljuset/kameran alltid vända mot en specificerad nod, detta är användbart i animation.

{{% alert color="primary" %}}

Klasserna [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) och [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) används i koden. För att spara en `Scene` används [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)-metoden, accepterar den ett filnamn med komplett sökväg och parameter [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat).

{{% /alert %}}

I exempel nedan är målet och kameran inställd i 3D:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-SetupTargetAndCamera-SetupTargetAndCamera.cs" >}}
