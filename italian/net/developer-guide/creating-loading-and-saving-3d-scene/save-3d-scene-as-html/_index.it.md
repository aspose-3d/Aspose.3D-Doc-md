---
title: Salva 3D Scena come HTML in C#
linktitle: Salva la scena 3D come HTML
type: docs
weight: 90
url: /it/net/save-3d-scene-as-html/
---
## **Panoramica**

Questo articolo spiega come è possibile convertire i file 3D a HTML dopo[Caricandoli nell'oggetto Scene](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/)Utilizzando C# e copre un'ampia gamma di argomenti (considerando[Formati di file supportati](https://docs.aspose.com/3d/net/supported-file-formats/)) Ad es.

- Convertire 3DS a HTML utilizzando C#
- Convertire fino allo FBX HTML nel C#
- Convertire fino allo STL HTML nel C#
- Convertire fino allo U3D HTML nel C#
- Convertire fino allo OBJ HTML nel C#


{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.9 o maggiore.

{{% /alert %}} 
## **Salva la scena 3D come HTML**
Aspose.3D for .NET fornisce la classe `Html5SaveOptions` per salvare una scena di salvataggio 3D come HTML. Quando si esporta la scena in un file HTML5, API esporterà tre file, un file `HTML`, un file DWeb Aspose3 (*.**A3dw**) E un file "JavaScript" reso. Per esportare solo file a3dw, è possibile specificare DWeb Aspose3 come tipo di esportazione e riutilizzare il file JavaScript all'interno della propria pagina HTML. Il seguente frammento di codice C# mostra come salvare una scena 3D come HTML.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-HtmlSaveOption.cs" >}}

{{% alert color="primary" %}} 

A causa dei limiti di sicurezza del browser, il file HTML esportato non può essere aperto direttamente, è necessario aprirlo tramite un server Web, se è installato python3, è possibile avviare il server Web nella riga di comando nella directory esportata

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Allora aprilo<http://localhost:8000/test.html>. Il renderer web utilizza WebGL2, è possibile utilizzare<https://get.webgl.org/webgl2/>Per verificare se il tuo browser lo supporta o meno.


