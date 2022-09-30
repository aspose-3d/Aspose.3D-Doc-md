---
title: Lägg till animationsegenskaper och inställningskamera i 3D dokument.
type: docs
weight: 10
url: /sv/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: I Aspose.3D, är objekt animation faktiskt nyckel-ram animation som animerar på egenskaper. För att animera egenskaper behöver du en CurveMapping instans som kartlägger komponenter i en egenskap till olika kurvor, till exempel, en Vector3-egenskap kan ha 3 komponenter X/Y/Z, som kommer att ställa upp tre kanaler i CurveMapping, Varje kanal kan ha en uppsättning av kurvor.
---
## **Lägg till animationsegenskaper i dokument 3D**
Aspose.3D for .NET stöder återgivning animerad scen. Den här artikeln förklarar förutsättningarna för att flytta ett föremål.
### **Flytta kubens position**
{{% alert color="primary" %}}

Klassobjektet [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) används i koden. Vi kan det.[Skapa ett Mesh-klassobjekt som berättat där.](/3d/sv/net/create-and-read-an-existing-3d-scene/)Och det måste animera den lokala översättning egenskapen av noden också:[Lägga till omvandlingen i noden](/3d/sv/net/adding-transformation-to-the-node/).

{{% /alert %}}

I Aspose.3D, är objekt animation faktiskt nyckel-ram animation som animerar på egenskaper. För att animera egenskaper behöver du en `CurveMapping` instans som kartlägger komponenter i en egenskap till olika kurvor, t.ex. a `Vector3` egendom kan ha 3 komponenter `X`/`Y`/`Z`, som kommer att inrätta tre kanaler i `CurveMapping`, varje kanal kan ha en uppsättning `Curve`.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-PropertyToDocument-AddAnimationPropertyToDocument.cs" >}}
## **Ställ in målkameran i 3D fil**
Aspose.3D for .NET erbjuder att ställa in målkameran i 3D fil. I vissa filformat, stöder ljus/kamera mål, vilket tillåter ljuset/kameran alltid vända mot en specificerad nod, detta är användbart i animation.

{{% alert color="primary" %}}

Klasserna [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) och [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) används i koden. För att spara en `Scene`, används [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) metod, det accepterar ett filnamn med komplett sökväg och [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat) parameter.

{{% /alert %}}

I exempel nedan är mål och kamera inställd i filen 3D:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-SetupTargetAndCamera-SetupTargetAndCamera.cs" >}}
