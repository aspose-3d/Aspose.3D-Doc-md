---
title: Crea una scena con forme primitive 3D
type: docs
weight: 10
url: /it/net/create-scene-with-primitive-3d-shapes/
description: Utilizzando Aspose.3D for .NET, gli sviluppatori possono definire una scena con forme primitive di 3D. Tutte le primitive parametrizzate verranno convertite automaticamente in mesh durante il salvataggio in qualsiasi formato di file di output supportato.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), gli sviluppatori possono definire una scena con forme primitive di 3D. Tutte le primitive parametrizzate verranno convertite automaticamente in mesh durante il salvataggio in qualsiasi formato di file di output supportato.

{{% /alert %}}
##  **Costruisci una scena dalle forme primitive 3D**
La modellazione è il processo di pura creazione e Aspose.3D API supporta la creazione di una scena con forme primitive di 3D.
###  **Campione di programmazione**
Questo esempio di codice crea una scena con forme primitive di 3D e salva nel file FBX.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.RootNode.CreateChildNode("box", new Box());
// Create a Cylinder model
scene.RootNode.CreateChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
scene.Save("test.fbx");


{{< /highlight >}}
