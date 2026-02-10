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

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();             

// Each cube node has their own translation
Node cube1 = scene.RootNode.CreateChildNode("cube1", mesh);

// Find translation property on node's transform object
Property translation = cube1.Transform.FindProperty("Translation");
            
// Create a bind point based on translation property
BindPoint bindPoint = new BindPoint(scene, translation);

// Create the animation curve on X component of the scale 
bindPoint.BindKeyframeSequence("X", new KeyframeSequence()
{
    // Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
    {0, 10.0f, Interpolation.Bezier},
    // Move node's translation to (20, 0, -10) at 3 sec
    {3, 20.0f, Interpolation.Bezier},
    // Move node's translation to (30, 0, 0) at 5 sec
    {5, 30.0f, Interpolation.Linear},
});

// Create the animation curve on Z component of the scale 
bindPoint.BindKeyframeSequence("Z", new KeyframeSequence()
{
    // Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
    {0, 10.0f, Interpolation.Bezier},
    // Move node's translation to (20, 0, -10) at 3 sec
    {3, -10.0f, Interpolation.Bezier},
    // Move node's translation to (30, 0, 0) at 5 sec
    {5, 0.0f, Interpolation.Linear},
});

// Save 3D scene in the supported file formats
scene.Save("PropertyToDocument.fbx");

{{< /highlight >}}
##  **Ställ in målkameran i 3D fil**
Aspose.3D for .NET erbjuder att ställa in målkameran i 3D-fil. I vissa filformat, stöder ljus/kamera mål, vilket tillåter ljuset/kameran alltid vända mot en specificerad nod, detta är användbart i animation.

{{% alert color="primary" %}}

Klasserna [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) och [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) används i koden. För att spara en `Scene` används [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)-metoden, accepterar den ett filnamn med komplett sökväg och parameter [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat).

{{% /alert %}}

I exempel nedan är målet och kameran inställd i 3D:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Get a child node object
Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());
// Set camera node translation
cameraNode.Transform.Translation = new Vector3(100, 20, 0);
cameraNode.GetEntity<Camera>().Target = scene.RootNode.CreateChildNode("target");
scene.Save("camera-test.3ds");

{{< /highlight >}}
