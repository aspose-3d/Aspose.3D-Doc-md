---
title: La tua prima domanda Aspose.3D
type: docs
weight: 30
url: /it/net/your-first-aspose-3d-application/
description: Crea, modifica e salva il tuo primo file 3d in qualsiasi formato supportato utilizzando Aspose.3D for .NET per provare la sua semplicità e potenza in C#.
keywords: C# , Aspose.3D for .NET , The first application using Aspose.3D for .NET, The first program via Aspose.3D for .NET.
---
{{% alert color="primary" %}}

Questo tutorial spiega come creare la tua prima applicazione utilizzando Aspose.3D semplici API. Questa semplice applicazione crea un file 3d in una scena 3D specificata.

{{% /alert %}}

##  **Come creare l'applicazione**

I passaggi seguenti creano l'applicazione utilizzando Aspose.3D API:

1. Crea un'istanza della classe [Scena](https://reference.aspose.com/3d/net/aspose.threed/scene/).
1. Se hai una licenza, allora [Applicalo](/3d/it/net/licensing/).
Se si utilizza la versione di valutazione, saltare le righe di codice relative alla licenza.
1. Crea un nuovo file 3D o apri un file 3D esistente.
1. Accedi ai contenuti della scena nel file 3D.
1. Generare il file 3D modificato.

L'implementazione dei passaggi precedenti è dimostrata negli esempi seguenti.

###  **Come creare un nuovo documento di scena**

L'esempio seguente crea un nuovo file di scena 3D da zero. Per prima cosa, crea una scena 3D e poi salva il file in formato FBX.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.Save("document.fbx");

{{< /highlight >}}

###  **Come aprire un file esistente**

L'esempio seguente apre un file modello esistente di 3D denominato "document.fbx" e quindi salva la scena o il documento 3D in uno streaming in vari formati 3D supportati.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
// Load a 3D document into Aspose.3D
Scene scene = new Scene();

// Open an existing 3D scene
scene.Open("document.fbx");

// Save Scene to a stream
MemoryStream dstStream = new MemoryStream();
scene.Save(dstStream, FileFormat.FBX7500ASCII);
            
// Save Scene to a local path
scene.Save("output_out.fbx");

{{< /highlight >}}
