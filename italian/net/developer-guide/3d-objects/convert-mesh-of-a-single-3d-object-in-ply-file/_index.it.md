---
title: Convertire Mesh di un singolo oggetto 3D in file PLY
type: docs
weight: 20
url: /it/net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: I membri EncodeMesh sovraccaricati esposti dalla classe PlyFormat possono essere utilizzati per convertire la mesh di un oggetto 3D in file PLY. I membri EncodeMesh prendono il nome mesh, il nome del file di output e gli oggetti PlySaveOptions come parametri. Utilizzando le opzioni di salvataggio PLY, gli sviluppatori possono modificare il nome dei componenti delle coordinate.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API consente agli sviluppatori di convertire la mesh di un singolo oggetto 3D nel file PLY.

{{% /alert %}}
##  **Crea un oggetto 3D e salvalo in un file PLY**
I membri sovraccarichi di `EncodeMesh` esposti dalla classe `PlyFormat` possono essere utilizzati per convertire `Mesh` di un oggetto 3D in un file PLY. I membri di `EncodeMesh` prendono come parametri `Mesh`, il nome del file di output e `PlySaveOptions` oggetti. Utilizzando le opzioni di salvataggio PLY, gli sviluppatori possono cambiare il nome dei componenti delle coordinate.
###  **Campione di programmazione**
Questo esempio di codice crea un oggetto Cilindro 3D, quindi codifica nel file PLY.

**C#**

{{< highlight "java" >}}

 // Create a cylinder object and save it to ply file

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply");

/* using Ply save options*/

//Save as binary PLY format, the default value is ASCII

PlySaveOptions opt = new PlySaveOptions(FileContentType.Binary);

//change the components to 's' and 't'

opt.TextureCoordinateComponents.Item1 = "s";

opt.TextureCoordinateComponents.Item2 = "t";

//save the mesh

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply", opt);

{{< /highlight >}}
