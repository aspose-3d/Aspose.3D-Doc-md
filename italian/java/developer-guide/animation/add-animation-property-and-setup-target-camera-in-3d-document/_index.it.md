---
title: Aggiungi proprietà di animazione e configurazione della fotocamera di destinazione nel documento 3D
type: docs
weight: 10
url: /it/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java supporta il rendering della scena animata. Questo articolo spiega i prerequisiti per spostare un oggetto.
---
##  **Aggiungi proprietà Animazione nel documento 3D**
Aspose.3D for Java supporta il rendering della scena animata. Questo articolo spiega i prerequisiti per spostare un oggetto.
###  **Sposta la posizione del cubo**
{{% alert color="primary" %}}

L'oggetto della classe `Mesh` viene utilizzato nel codice. Possiamo [Creare un oggetto classe Mesh come narrato lì](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) ed è necessario animare anche la proprietà di traduzione locale del nodo: [Aggiunta della trasformazione al nodo](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D for Java API, l'istanza di animazione è in realtà un'animazione con fotogrammi chiave che anima le proprietà. Per animare le proprietà, hai bisogno di un'istanza `CurveMapping` che mappa i componenti di una proprietà a curve diverse, ad esempio, una proprietà `Vector3` può avere 3 componenti `X`/`Y`/`Z`, che imposterà tre canali in `CurveMapping`, ogni canale può avere un set di `Curve`.

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
##  **Configurazione della fotocamera di destinazione nel file 3D**
Aspose.3D for Java offre la configurazione della fotocamera di destinazione in 3D file. In alcuni formati di file, la luce/la fotocamera supporta il target, che consente alla luce/fotocamera di affrontare sempre un nodo specificato, questo è utile nell'animazione.

{{% alert color="primary" %}}

Le classi `Scene`, `Camera`, `Node` e `Transform` vengono utilizzate nel codice. Per risparmiare un metodo `Scene`, `Scene.save`, accetta un nome file con percorso completo e un parametro `FileFormat`.

{{% /alert %}}

Nell'esempio seguente, la destinazione e la fotocamera sono configurate nel file 3D:

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
