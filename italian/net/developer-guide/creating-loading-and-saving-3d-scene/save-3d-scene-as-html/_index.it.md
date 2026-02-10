---
title: Risparmia 3D Scena come HTML in C#
linktitle: Risparmia 3D Scena come HTML
type: docs
weight: 90
url: /it/net/save-3d-scene-as-html/
---
##  **Panoramica**

Questo articolo spiega come puoi convertire i file 3D in HTML dopo [Caricandoli nell'oggetto Scene](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) utilizzando C# e copre un'ampia gamma di argomenti (considerando [Formati di file supportati](https://docs.aspose.com/3d/net/supported-file-formats/)) ad es.

- Converti 3DS in HTML utilizzando C#
- Convertire FBX in HTML in C#
- Convertire STL in HTML in C#
- Convertire U3D in HTML in C#
- Convertire OBJ in HTML in C#


{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.9 o maggiore.

{{% /alert %}} 
##  **Risparmia 3D Scena come HTML**
Aspose.3D for .NET offre `Html5SaveOptions` di classe per salvare una scena di 3D di risparmio come HTML. Quando esporti la scena in file HTML5, API esporterà tre file, un file `HTML`, un file DWeb Aspose3 (*.* a3dw **) e un file `JavaScript` reso. Per esportare solo file a3dw, è possibile specificare Aspose3DWeb come tipo di esportazione e riutilizzare il file JavaScript all'interno della propria pagina HTML. Il seguente frammento di codice C# mostra come salvare una scena 3D come HTML.



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize 3D scene
var scene = new Scene();
// Create a child node
var node = scene.RootNode.CreateChildNode(new Cylinder());
// Set child node properites
node.Material = new LambertMaterial() { DiffuseColor = new Vector3(Color.Chartreuse) };
scene.RootNode.CreateChildNode(new Light() { LightType = LightType.Point }).Transform.Translation = new Vector3(10, 0, 10);
// Create a Html5SaveOptions
var opt = new Html5SaveOptions();
//Turn off the grid
opt.ShowGrid = false;
//Turn off the user interface
opt.ShowUI = false; 
// Save 3D to HTML5
scene.Save("HtmlSaveOption.html", opt);

{{< /highlight >}}

{{% alert color="primary" %}} 

A causa dei limiti di sicurezza del browser, il file HTML esportato non può essere aperto direttamente, è necessario aprirlo tramite un server Web, se è installato python3, è possibile avviare il server Web nella riga di comando nella directory esportata

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Allora aprilo<http://localhost:8000/test.html>. Il renderer web utilizza WebGL2, è possibile utilizzare<https://get.webgl.org/webgl2/>Per verificare se il tuo browser lo supporta o meno.


