---
title: Specificare 3D Opzioni di caricamento file in C#
linktitle: Specificare 3D Opzioni di caricamento file
type: docs
weight: 30
url: /it/net/specify-3d-file-load-options/
description: Esistono diversi overload del metodo Scene.Open o overload del costruttore di classi Scene che accettano un oggetto LoadOptions. Ogni formato di carico ha una classe corrispondente che contiene le opzioni di carico per quel formato di carico.
---
##  **Panoramica**

Questo articolo spiega come è possibile caricare diversi tipi di file 3D utilizzando le rispettive classi di opzioni di carico in C# all'interno dell'oggetto Scena e quindi è possibile [Salvarlo in diversi formati di file supportati da 3D](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). Caricando e salvando, puoi eseguire il numero di conversioni diverse, ad es.

- Convertire FBX in OBJ in C#
- Convertire 3DS in FBX in C#
- Convertire U3D in OBJ in C#
- Convertire OBJ in 3DS in C#
- Converti da X a 3DS in C#

##  **3D Opzioni di caricamento file**
Sono disponibili diversi overload del metodo [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) o overload del costruttore di classi Scene che accettano un oggetto `LoadOptions`. Questo dovrebbe essere un oggetto di una classe derivata dalla classe `LoadOptions`. Ogni formato di carico ha una classe corrispondente che contiene le opzioni di carico per quel formato di carico, ad esempio c' è `ColladaSaveOptions` per il formato di salvataggio `FileFormat.Collada`.
###  **Utilizzo delle opzioni di carico discre 3DS**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un file Discreet 3DS.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
###  **Utilizzo delle opzioni di carico Obj**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un file Obj 3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
###  **Utilizzo delle opzioni di carico STL**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un file STL.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
###  **Utilizzo delle opzioni di carico U3D**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un file U3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
###  **Utilizzo delle opzioni di carico glTF**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un file glTF.
####  **Capovolgi la Coordinata texture V/T**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
###  **Utilizzo delle opzioni di carico Ply**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un modello PLY.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
###  **Utilizzo delle opzioni di carico DirectX X**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un file DirectX X.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
###  **Utilizza RVM opzioni di carico**
**C#**

{{< highlight "java" >}}

 // set load options of RVM

Scene scene = new Scene();

var opt = new RvmLoadOptions()

{

    CylinderRadialSegments = 32,

    DishLatitudeSegments = 16,

    DishLongitudeSegments = 24,

    TorusTubularSegments = 40

};

// import RVM

scene.Open("LAD-TOP.rvm", opt);

// save in the OBJ format

scene.Save("LAD-TOP.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
###  **Utilizzo di FBX opzioni di carico**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
