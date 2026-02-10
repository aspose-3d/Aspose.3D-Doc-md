---
title: La tua prima domanda Aspose.3D
type: docs
weight: 30
url: /it/java/your-first-aspose-3d-application/
description: Crea, modifica e salva il tuo primo file 3d in qualsiasi formato supportato utilizzando Aspose.3D for Java per provare la sua semplicità e potenza in Java.
keywords: Java , Aspose.3D for Java , The first application using Aspose.3D for Java, The first program via Aspose.3D for Java.
---
{{% alert color="primary" %}}

Questo tutorial spiega come creare la tua prima applicazione utilizzando Aspose.3D semplici API. Questa semplice applicazione crea un file 3d in una scena 3D specificata.

{{% /alert %}}

##  **Come creare l'applicazione**

I passaggi seguenti creano l'applicazione utilizzando Aspose.3D API:

1. Crea un'istanza della classe [Scena](https://reference.aspose.com/3d/java/com.aspose.threed/scene/).
1. Se hai una licenza, allora [Applicalo](/3d/it/java/licensing/).
Se si utilizza la versione di valutazione, saltare le righe di codice relative alla licenza.
1. Crea un nuovo file 3D o apri un file 3D esistente.
1. Accedi ai contenuti della scena nel file 3D.
1. Generare il file 3D modificato.

L'implementazione dei passaggi precedenti è dimostrata negli esempi seguenti.

###  **Come creare un nuovo documento di scena**

L'esempio seguente crea un nuovo file di scena 3D da zero. Per prima cosa, crea una scena 3D e poi salva il file in formato FBX.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "document.fbx";
// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}

###  **Come aprire un file esistente**

L'esempio seguente apre un file modello esistente di 3D denominato "document.fbx" e quindi salva la scena o il documento 3D in uno streaming in vari formati 3D supportati.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load a 3D document into Aspose.3D
Scene scene = new Scene();
// Open an existing 3D scene
scene.open(MyDir + "document.fbx");
// Save Scene to a stream
try (MemoryStream dstStream = new MemoryStream()) {
    scene.save(dstStream, FileFormat.FBX7500ASCII);
}
// Save Scene to a local path
scene.save(MyDir + "output_out.fbx", FileFormat.FBX7500ASCII);
{{< /highlight >}}
