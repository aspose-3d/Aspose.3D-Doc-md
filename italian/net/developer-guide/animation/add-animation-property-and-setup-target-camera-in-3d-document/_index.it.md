---
title: Aggiungere proprietà di animazione e impostare la fotocamera di destinazione nel documento 3D
type: docs
weight: 10
url: /it/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: Nello Aspose.3D, l'animazione dell'oggetto è in realtà un'animazione key-frame che anima le proprietà. Per animare le proprietà, è necessaria un'istanza CurveMapping che mappa i componenti di una proprietà a curve diverse, ad esempio, una proprietà Vector3 può avere 3 componenti X/Y/Z, che imposteranno tre canali in CurveMapping, ogni canale può avere un insieme di curve.
---
## **Aggiungi proprietà Animazione nel documento 3D**
Aspose.3D for .NET supporta il rendering della scena animata. Questo articolo spiega i prerequisiti per spostare un oggetto.
### **Sposta la posizione del cubo**
{{% alert color="primary" %}}

L'oggetto della classe [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) viene utilizzato nel codice. Possiamo[Creare un oggetto classe Mesh come narrato lì](/3d/it/net/create-and-read-an-existing-3d-scene/)Ed è necessario animare anche la proprietà di traduzione locale del nodo:[Aggiunta della trasformazione al nodo](/3d/it/net/adding-transformation-to-the-node/).

{{% /alert %}}

Nello Aspose.3D, l'animazione dell'oggetto è in realtà un'animazione key-frame che anima le proprietà. Per animare le proprietà, è necessaria un'istanza `CurveMapping` che mappa i componenti di una proprietà a curve diverse, ad esempio, una proprietà `Vector3` può avere 3 componenti `X`/`Y`/`Z`, che imposterà tre canali nello `CurveMapping`, ogni canale può avere un set di `Curve`.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-PropertyToDocument-AddAnimationPropertyToDocument.cs" >}}
## **Configurazione della fotocamera di destinazione nel file 3D**
Aspose.3D for .NET offre la configurazione della fotocamera di destinazione nel file 3D. In alcuni formati di file, la luce/la fotocamera supporta il target, che consente alla luce/fotocamera di affrontare sempre un nodo specificato, questo è utile nell'animazione.

{{% alert color="primary" %}}

Le classi [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) e [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) vengono utilizzate nel codice. Per salvare un metodo `Scene`, [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) viene utilizzato, accetta un nome file con percorso completo e parametro [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat).

{{% /alert %}}

Nell'esempio seguente, la destinazione e la fotocamera sono configurate nel file 3D:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-SetupTargetAndCamera-SetupTargetAndCamera.cs" >}}
