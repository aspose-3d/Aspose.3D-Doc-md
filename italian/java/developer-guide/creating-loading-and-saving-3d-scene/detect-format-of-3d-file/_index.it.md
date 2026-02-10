---
title: Rileva il formato del file 3D
type: docs
weight: 10
url: /it/java/detect-format-of-3d-file/
description: Aspose.3D for Java API supporta il rilevamento di 3D formati supportati prima dell'apertura perché l'estensione del file non garantisce che il contenuto del file sia appropriato.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API supporta il rilevamento di 3D formati supportati prima dell'apertura perché l'estensione del file non garantisce che il contenuto del file sia appropriato.

{{% /alert %}} 
##  **Rileva il campione di programmazione del formato**
Questo codice sorgente illustra come rilevare il formato del file (utilizzando il percorso o il flusso del file) e controllarne l'estensione.

{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// detect format of 3D file
FileFormat inputFormat = FileFormat.detect(MyDir + "document.fbx");
// display the file format
System.out.println("File Format: " + inputFormat.toString());
{{< /highlight >}}




