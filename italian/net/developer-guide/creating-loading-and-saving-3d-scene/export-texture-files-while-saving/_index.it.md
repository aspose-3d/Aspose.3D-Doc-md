---
title: Esporta file di texture durante il salvataggio della scena 3D
type: docs
weight: 10
url: /it/net/export-texture-files-while-saving-3d-scene
description: Utilizzando Aspose.3D for .NET, gli sviluppatori possono esportare file di texture nel file system salvando 3D scena.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), Quando si esporta una scena in file, spesso è necessario esportare le trame, incorporate o esterne, nella stessa directory. Aspose.3D for .NET facilita questo processo, assicurando che tutte le trame siano gestite e archiviate correttamente insieme alla scena esportata. Questa guida dimostra come raggiungere questo obiettivo.

{{% /alert %}}

Per esportare una scena e assicurarsi che tutte le trame associate vengano salvate nella stessa directory, segui questi passaggi:


{{% highlight "csharp" %}}

Scene scene = Scene.FromFile(@"BoomBox.glb");
var opt = new ObjSaveOptions();
opt.ExportTextures = true;
scene.Save(@"D:\tmp\boombox\output.obj", opt);

{{% /highlight %}}


Tutti gli oggetti `SaveOptions` in Aspose.3D includono la proprietà `ExportTextures`, che semplifica il processo di gestione delle trame durante l'esportazione. Questa proprietà garantisce che tutte le trame, sia esterne che incorporate, vengano salvate nella directory di output specificata. Questa funzione è compatibile con vari formati di file che supportano l'esportazione di texture, come FBX, 3DS, OBJ, USD, GLTF e DAE.



Spiegazione

1. Caricare la scena: La scena viene caricata dal file di input.
1. Configura le opzioni di salvataggio: imposta `ExportTextures` su `true`.
1. Esporta la scena: la scena viene salvata nella directory di output con i percorsi di texture aggiornati.


Sfruttando la proprietà `ExportTextures` in `SaveOptions`, puoi esportare senza problemi 3D scene insieme alle loro trame, assicurandoti che tutte le risorse necessarie siano organizzate in un'unica directory. Questa funzione migliora la portabilità e la facilità d'uso dei file 3D su varie piattaforme e applicazioni.

##  **Risorse**

1. [Tutorial online](https://products.aspose.com/3d/tutorial/)
1. [Opzioni di salvataggio](https://reference.aspose.com/3d/net/aspose.threed.formats/saveoptions/)
