---
title: Crea una scena con forme primitive 3D
type: docs
weight: 10
url: /it/python-net/create-scene-with-primitive-3d-shapes/
description: Utilizzando Aspose.3D for Python via .NET, gli sviluppatori possono definire una scena con forme primitive di 3D. Tutte le primitive parametrizzate verranno convertite automaticamente in mesh durante il salvataggio in qualsiasi formato di file di output supportato.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), gli sviluppatori possono definire una scena con forme primitive di 3D. Tutte le primitive parametrizzate verranno convertite automaticamente in mesh durante il salvataggio in qualsiasi formato di file di output supportato.

{{% /alert %}}
##  **Costruisci una scena dalle forme primitive 3D**
La modellazione è il processo di pura creazione e Aspose.3D API supporta la creazione di una scena con forme primitive di 3D.
###  **Campione di programmazione**
Questo esempio di codice crea una scena con forme primitive di 3D e salva nel file FBX.

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Box, Cylinder

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
#  Initialize a Scene object
scene = Scene()
#  Create a Box model
scene.root_node.create_child_node("box", Box())
#  Create a Cylinder model
scene.root_node.create_child_node("cylinder", Cylinder())
#  Save drawing in the FBX format
output = "out"  + "test.fbx"
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
