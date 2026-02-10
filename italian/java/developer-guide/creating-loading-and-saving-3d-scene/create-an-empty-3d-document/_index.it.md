---
title: Crea un documento vuoto 3D
type: docs
weight: 20
url: /it/java/create-an-empty-3d-document/
description: Aspose.3D for Java API supporta la creazione di 3D da zero, quindi risparmia nel formato 3D supportato.
---
##  **Crea una scena vuota 3D e risparmia in formato 3D supportato**
Aspose.3D for Java API supporta la creazione di 3D da zero, quindi risparmia nel formato 3D supportato.
###  **Creazione di una scena vuota 3D**
Segui questi passaggi per creare una scena 3D con Aspose.3D for Java API:

1. Creare un'istanza dell'**Scena**Classe che rappresenta 3D scena.
1. Generare 3D documento chiamando il**Salva**Metodo della**Scena**Istanza di classe.
####  **Creazione di una scena vuota 3D: campioni di programmazione**
{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "document.fbx";
// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}




