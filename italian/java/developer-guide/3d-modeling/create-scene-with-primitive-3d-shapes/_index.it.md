---
title: Crea una scena con forme primitive 3D
type: docs
weight: 20
url: /it/java/create-scene-with-primitive-3d-shapes/
description: Aspose.3D for Java API supporta forme primitive di 3D. Tutte le primitive parametrizzate verranno convertite automaticamente in mesh durante il salvataggio in qualsiasi formato di file di output supportato.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API supporta forme primitive di 3D. Tutte le primitive parametrizzate verranno convertite automaticamente in mesh durante il salvataggio in qualsiasi formato di file di output supportato.

{{% /alert %}} 
##  **Costruisci una scena dalle forme primitive 3D**
La modellazione è il processo di pura creazione e Aspose.3D API supporta la creazione di una scena con forme primitive di 3D.
###  **Campione di programmazione**
Questo esempio di codice crea una scena con forme primitive di 3D e salva nel file FBX.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.getRootNode().createChildNode("box", new Box());
// Create a Cylinder model
scene.getRootNode().createChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
MyDir = MyDir + RunExamples.getOutputFilePath("test.fbx");
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
