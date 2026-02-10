---
title: Animasyon özelliği ve kurulum hedef kamerayı 3D belgesine ekleyin
type: docs
weight: 10
url: /tr/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D, nesne animasyonu aslında özellikler üzerinde animasyonlar yapan anahtar çerçeve animasyonudur. Özellikleri canlandırmak için, bir mülkün bileşenlerini farklı eğrilere eşleştiren bir eğrileme örneğine ihtiyacınız vardır, örneğin, bir vector3 özelliği, üç kanalı eğrilemede kuracak 3 bileşen x/y/z'ye sahip olabilir, her kanal bir eğri kümesine sahip olabilir.
---
##  **Animasyon özelliğini 3D belgesine ekleyin**
Aspose.3D for .NET animasyonlu sahne oluşturmayı destekler. Bu makale, bir nesneyi taşımak için ön şartları açıklar.
###  **Move Cube's Position**
{{% alert color="primary" %}}

The [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) class object is being used in the code. We can [create a Mesh class object as narrated there](/3d/net/create-and-read-an-existing-3d-scene/) and it's must animate the local translation property of the node too: [Adding the Transformation to the Node](/3d/net/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D, object animation is actually key-frame animation that animates on properties. To animate properties, you need a `CurveMapping` instance which maps components of a property to different curves, for example, a `Vector3` property can have 3 components `X`/`Y`/`Z`, which will set up three channels in `CurveMapping`, every channel can have a set of `Curve`.

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
##  **Hedef kamerayı 3D dosyasında kur**
Aspose.3D for .NET offers to setup the target camera in 3D file. In some file formats, light/camera supports target, which allows the light/camera always facing a specified node, this is useful in animation.

{{% alert color="primary" %}}

[`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) ve [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) sınıfları kodda kullanılıyor. `Scene`, [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) yöntemini kaydetmek için, tam yol ve [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat) parametresi olan bir dosya adını kabul eder.

{{% /alert %}}

Aşağıdaki örnekte, hedef ve kamera 3D dosyasında kurulur:

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
