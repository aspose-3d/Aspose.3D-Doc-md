---
title: Aggiungi proprietà di animazione e configurazione della fotocamera di destinazione nel documento 3D
type: docs
weight: 10
url: /it/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: In Aspose.3D, l'animazione dell'oggetto è in realtà un'animazione con fotogrammi chiave che anima le proprietà. Per animare le proprietà, è necessaria un'istanza CurveMapping che mappa i componenti di una proprietà a curve diverse, ad esempio, una proprietà Vector3 può avere 3 componenti X/Y/Z, che imposteranno tre canali in CurveMapping, ogni canale può avere un insieme di curve.
---
##  **Aggiungi proprietà Animazione nel documento 3D**
Aspose.3D for .NET supporta il rendering della scena animata. Questo articolo spiega i prerequisiti per spostare un oggetto.
###  **Sposta la posizione del cubo**
{{% alert color="primary" %}}

L'oggetto della classe [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) viene utilizzato nel codice. Possiamo [Creare un oggetto classe Mesh come narrato lì](/3d/it/net/create-and-read-an-existing-3d-scene/) ed è necessario animare anche la proprietà di traduzione locale del nodo: [Aggiunta della trasformazione al nodo](/3d/it/net/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D, l'animazione dell'oggetto è in realtà un'animazione con fotogrammi chiave che anima le proprietà. Per animare le proprietà, hai bisogno di un'istanza `CurveMapping` che mappa i componenti di una proprietà a curve diverse, ad esempio, una proprietà `Vector3` può avere 3 componenti `X`/`Y`/`Z`, che imposterà tre canali in `CurveMapping`, ogni canale può avere un set di `Curve`.

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
##  **Configurazione della fotocamera di destinazione nel file 3D**
Aspose.3D for .NET offre la configurazione della fotocamera di destinazione in 3D file. In alcuni formati di file, la luce/la fotocamera supporta il target, che consente alla luce/fotocamera di affrontare sempre un nodo specificato, questo è utile nell'animazione.

{{% alert color="primary" %}}

Le classi [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) e [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) vengono utilizzate nel codice. Per salvare un metodo `Scene`, [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save), accetta un nome file con percorso completo e un parametro [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat).

{{% /alert %}}

Nell'esempio seguente, la destinazione e la fotocamera sono configurate nel file 3D:

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
