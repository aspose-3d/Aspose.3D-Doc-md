---
title: Aggiungere proprietà di animazione e impostare la fotocamera di destinazione nel documento 3D
type: docs
weight: 10
url: /it/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java supporta il rendering della scena animata. Questo articolo spiega i prerequisiti per spostare un oggetto.
---
## **Aggiungi proprietà Animazione nel documento 3D**
Aspose.3D for Java supporta il rendering della scena animata. Questo articolo spiega i prerequisiti per spostare un oggetto.
### **Sposta la posizione del cubo**
{{% alert color="primary" %}}

L'oggetto della classe `Mesh` viene utilizzato nel codice. Possiamo[Creare un oggetto classe Mesh come narrato lì](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/)Ed è necessario animare anche la proprietà di traduzione locale del nodo:[Aggiunta della trasformazione al nodo](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D for Java API, l'istanza dell'animazione è in realtà un'animazione key-frame che anima sulle proprietà. Per animare le proprietà, è necessaria un'istanza `CurveMapping` che mappa i componenti di una proprietà a curve diverse, ad esempio, una proprietà `Vector3` può avere 3 componenti `X`/`Y`/`Z`, che imposterà tre canali nello `CurveMapping`, ogni canale può avere un set di `Curve`.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
## **Configurazione della fotocamera di destinazione nel file 3D**
Aspose.3D for Java offre la configurazione della fotocamera di destinazione nel file 3D. In alcuni formati di file, la luce/la fotocamera supporta il target, che consente alla luce/fotocamera di affrontare sempre un nodo specificato, questo è utile nell'animazione.

{{% alert color="primary" %}}

Le classi `Scene`, `Camera`, `Node` e `Transform` vengono utilizzate nel codice. Per salvare un metodo `Scene`, `Scene.save`, accetta un nome file con percorso completo e parametro `FileFormat`.

{{% /alert %}}

Nell'esempio seguente, la destinazione e la fotocamera sono configurate nel file 3D:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
