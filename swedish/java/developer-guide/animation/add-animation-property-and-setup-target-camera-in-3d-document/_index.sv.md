---
title: Lägg till animeringsegenskaper och inställningskamera i dokumentet 3D.
type: docs
weight: 10
url: /sv/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java stöder att visa animerad scen. Den här artikeln förklarar förutsättningarna för att flytta ett föremål.
---
##  **Add Animation property in 3D document**
Aspose.3D for Java stöder att visa animerad scen. Den här artikeln förklarar förutsättningarna för att flytta ett föremål.
###  **Flytta kubens position**
{{% alert color="primary" %}}

Klassobjektet `Mesh` används i koden. Vi kan [Skapa ett Mesh-klassobjekt som berättat där.](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) och det måste animera den lokala översättningsegenskapen för noden också: [Lägga till omvandlingen i noden](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

I Aspose.3D for Java API är animationsinstans i själva verket nyckelramanimation som animerar på egenskaper. För att animera egenskaper, behöver du en `CurveMapping` instans som kartlägger komponenter i en egenskap till olika kurvor, t.ex. en `Vector3` egenskap kan ha 3 komponenter `X`/`Y`/`Z`, som kommer att ställa in tre kanaler i `CurveMapping`, varje kanal kan ha en uppsättning `Curve`.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
##  **Ställ in målkameran i 3D fil**
Aspose.3D for Java erbjuder att ställa in målkameran i 3D-fil. I vissa filformat, stöder ljus/kamera mål, vilket tillåter ljuset/kameran alltid vända mot en specificerad nod, detta är användbart i animation.

{{% alert color="primary" %}}

Klasserna `Scene`, `Camera`, `Node` och `Transform` används i koden. För att spara en `Scene` används `Scene.save` metoden, det accepterar ett filnamn med komplett sökväg och `FileFormat` parameter.

{{% /alert %}}

I exempel nedan är målet och kameran inställd i 3D:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
