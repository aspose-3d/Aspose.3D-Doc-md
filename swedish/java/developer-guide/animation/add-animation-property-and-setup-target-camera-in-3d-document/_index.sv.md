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

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize scene object
Scene scene = new Scene();

// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();

// Each cube node has their own translation
Node cube1 = scene.getRootNode().createChildNode("cube1", mesh);

// Find translation property on node's transform object
Property translation = cube1.getTransform().findProperty("Translation");

// Create a bind point based on translation property
BindPoint bindPoint = new BindPoint(scene, translation);

// Create the animation curve on X component of the scale
KeyframeSequence kfs = new KeyframeSequence();
// Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
kfs.add(0, 10.0f, Interpolation.BEZIER);
// Move node's translation to (20, 0, -10) at 3 sec
kfs.add(3, 20.0f, Interpolation.BEZIER);
// Move node's translation to (30, 0, 0) at 5 sec
kfs.add(5, 30.0f, Interpolation.LINEAR);
            
bindPoint.bindKeyframeSequence("X", kfs);

kfs = new  KeyframeSequence();
// Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
kfs.add(0, 10.0f, Interpolation.BEZIER);
// Move node's translation to (20, 0, -10) at 3 sec
kfs.add(3, -10.0f, Interpolation.BEZIER);
// Move node's translation to (30, 0, 0) at 5 sec
kfs.add(5, 0.0f, Interpolation.LINEAR);
            
bindPoint.bindKeyframeSequence("Z", kfs);

// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("PropertyToDocument.fbx");

// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);

{{< /highlight >}}
##  **Ställ in målkameran i 3D fil**
Aspose.3D for Java erbjuder att ställa in målkameran i 3D-fil. I vissa filformat, stöder ljus/kamera mål, vilket tillåter ljuset/kameran alltid vända mot en specificerad nod, detta är användbart i animation.

{{% alert color="primary" %}}

Klasserna `Scene`, `Camera`, `Node` och `Transform` används i koden. För att spara en `Scene` används `Scene.save` metoden, det accepterar ett filnamn med komplett sökväg och `FileFormat` parameter.

{{% /alert %}}

I exempel nedan är målet och kameran inställd i 3D:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize scene object
Scene scene = new Scene();
// Get a child node object
Node cameraNode = scene.getRootNode().createChildNode("camera", new Camera());
// Set camera node translation
cameraNode.getTransform().setTranslation(new Vector3(100, 20, 0));
((Camera)cameraNode.getEntity()).setTarget(scene.getRootNode().createChildNode("target"));
MyDir = MyDir + "camera-test.3ds";
scene.save(MyDir, FileFormat.DISCREET3DS);
{{< /highlight >}}
