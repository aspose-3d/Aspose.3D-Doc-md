---
title: Risparmia 3D Scena come HTML
type: docs
weight: 70
url: /it/nodejs-java/save-3d-scene-as-html/
description: Aspose.3D for Node.js via Java fornisce la classe ** HtmlSaveOptions ** per salvare una scena di risparmio 3D come HTML.
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.9 o maggiore.

{{% /alert %}} 
#  **Risparmia 3D Scena come HTML**
Aspose.3D for Node.js via Java offre una classe `HtmlSaveOptions` per salvare una scena di 3D di risparmio come HTML. Quando esporti la scena in file HTML5, API esporterà tre file, un file `HTML`, un file DWeb Aspose3 (*.* a3dw **) e un file `JavaScript` reso. Per esportare solo file a3dw, è possibile specificare Aspose3DWeb come tipo di esportazione e riutilizzare il file JavaScript all'interno della propria pagina HTML. Il seguente frammento di codice mostra come salvare una scena di 3D come HTML.

{{< highlight "java" >}}

// Initialize a scene
var scene = new aspose.threed.Scene();

scene.getRootNode().createChildNode(new aspose.threed.Cylinder());

var opt =new aspose.threed.Html5SaveOptions();
// Turn off the grid
opt.setShowGrid(false);
//Turn off the user interface
opt.setShowUI(false);

scene.save("html5SaveOption.html);

{{< /highlight >}}


{{% alert color="primary" %}} 

A causa dei limiti di sicurezza del browser, il file HTML esportato non può essere aperto direttamente, è necessario aprirlo tramite un server Web, se è installato python3, è possibile avviare il server Web nella riga di comando nella directory esportata

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Allora aprilo<http://localhost:8000/test.html>. Il renderer web utilizza WebGL2, è possibile utilizzare<https://get.webgl.org/webgl2/>Per verificare se il tuo browser lo supporta o meno.


