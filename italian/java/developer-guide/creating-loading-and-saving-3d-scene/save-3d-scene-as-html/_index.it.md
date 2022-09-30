---
title: Salva la scena 3D come HTML
type: docs
weight: 70
url: /it/java/save-3d-scene-as-html/
description: Aspose.3D for Java fornisce la classe ** HtmlSaveOptions ** per salvare una scena di salvataggio 3D come HTML.
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.9 o maggiore.

{{% /alert %}} 
# **Salva la scena 3D come HTML**
Aspose.3D for Java fornisce la classe `HtmlSaveOptions` per salvare una scena di salvataggio 3D come HTML. Quando si esporta la scena in un file HTML5, API esporterà tre file, un file `HTML`, un file DWeb Aspose3 (*.**A3dw**) E un file "JavaScript" reso. Per esportare solo file a3dw, è possibile specificare DWeb Aspose3 come tipo di esportazione e riutilizzare il file JavaScript all'interno della propria pagina HTML. Il seguente frammento di codice mostra come salvare una scena 3D come HTML.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-html5SaveOption.java" >}}

{{% alert color="primary" %}} 

A causa dei limiti di sicurezza del browser, il file HTML esportato non può essere aperto direttamente, è necessario aprirlo tramite un server Web, se è installato python3, è possibile avviare il server Web nella riga di comando nella directory esportata

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Allora aprilo<http://localhost:8000/test.html>. Il renderer web utilizza WebGL2, è possibile utilizzare<https://get.webgl.org/webgl2/>Per verificare se il tuo browser lo supporta o meno.


