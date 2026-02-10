---
title: Upptäck format för 3D-filen
type: docs
weight: 10
url: /sv/java/detect-format-of-3d-file/
description: Aspose. 3D for Java API har stöd för att upptäcka 3D stödda format innan det öppnas eftersom filändelsen inte garanterar att filens innehåll är lämpligt.
---
{{% alert color="primary" %}} 

Aspose. 3D for Java API har stöd för att upptäcka 3D stödda format innan det öppnas eftersom filändelsen inte garanterar att filens innehåll är lämpligt.

{{% /alert %}} 
##  **Detektera formatprogrammeringsprover**
Denna källkod illustrerar hur man upptäcker filformatet (med hjälp av fil sökvägen eller strömmen) och kontrollera dess tillägg.

{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// detect format of 3D file
FileFormat inputFormat = FileFormat.detect(MyDir + "document.fbx");
// display the file format
System.out.println("File Format: " + inputFormat.toString());
{{< /highlight >}}




