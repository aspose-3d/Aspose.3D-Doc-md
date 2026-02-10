---
title: Codifica 3D mesh nel file Google Draco
type: docs
weight: 30
url: /it/java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Java API supporta l'importazione del modello 3D, recuperare la mesh e quindi codificare la mesh nel file Google Draco.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API supporta l'importazione del modello 3D, recuperare la mesh e quindi codificare la mesh nel file Google Draco. Gli sviluppatori possono anche specificare la posizione, le coordinate della trama, il colore e i bit normali, nonché il livello di compressione prima di codificare una mesh.

{{% /alert %}} 
##  **Recupera 3D Mesh e codifica in Google Draco File**
Il metodo di codifica esposto dalla classe `DracoFormat` può essere utilizzato per codificare una mesh 3D nel file Google Draco. Ci vogliono oggetti `Mesh` e `DracoSaveOptions` come parametri. Con le opzioni di salvataggio di Draco, gli sviluppatori possono anche specificare la posizione, le coordinate della trama, il colore e i bit normali, nonché il livello di compressione prima di codificare una mesh.
###  **Campione di programmazione**
Questo esempio di codice recupera Mesh of Sphere e quindi codifica nel file Google Draco dopo aver specificato un livello di compressione.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Create a sphere
Sphere sphere = new Sphere();
// Encode the sphere to Google Draco raw data using optimal compression level.
DracoSaveOptions opt = new DracoSaveOptions();
opt.setCompressionLevel(DracoCompressionLevel.OPTIMAL);
byte[] b = FileFormat.DRACO.encode(sphere.toMesh(), opt);
// Save the raw bytes to file
Files.write(Paths.get(MyDir, "SphereMeshtoDRC_Out.drc"), b);
{{< /highlight >}}
