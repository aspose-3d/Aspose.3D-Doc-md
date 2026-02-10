---
title: Salva un documento 3D in diversi formati 3D utilizzando C#
linktitle: Salva un documento 3D
type: docs
weight: 20
url: /it/net/save-a-3d-document/
description: La classe Scene di Aspose.3D API rappresenta un documento 3D e gli sviluppatori possono salvare il suo oggetto in qualsiasi formato di file supportato.
---
##  **Panoramica**
L'articolo spiega come salvare il documento 3D in vari formati utilizzando la libreria di elaborazione dei documenti C# 3D, tra cui

- Salva un documento 3D in formato FBX utilizzando C# - AutoDesk
- Risparmia un documento 3D in formato DAE utilizzando C# - Collada
- Salva un documento 3D in formato 3DS utilizzando C# - Discreet 3D Studio
- Risparmia un documento 3D in formato DRC utilizzando C# - Google Draco

{{% alert color="primary" %}} 

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) di Aspose.3D API rappresenta un documento 3D e gli sviluppatori possono salvare il suo oggetto in qualsiasi formato di file supportato. Per salvare una scena 3D, utilizza semplicemente il metodo [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save), accetta un nome file con percorso completo o un oggetto di flusso di file. Aspose.3D API offre un altro parametro `FileFormat` per specificare il formato del file di output.

{{% /alert %}} 

##  **Salva una scena 3D in formati 3D supportati**

Il codice di esempio C# di seguito mostra come salvare una scena o un documento 3D in uno streaming in vari formati 3D supportati.

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
