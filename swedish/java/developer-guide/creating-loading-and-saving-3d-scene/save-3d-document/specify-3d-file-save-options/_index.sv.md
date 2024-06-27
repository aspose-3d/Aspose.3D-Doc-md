---
title: Ange 3D Filspararalternativ
type: docs
weight: 10
url: /sv/java/specify-3d-file-save-options/
description: Det finns flera Scene.save metod överbelastningar som accepterar en SaveOptions instans.
---
##  **3D Filspararalternativ**
Det finns flera Scene.save metod överbelastningar som accepterar en SaveOptions instans. Detta bör vara en instans av en klass som härrör från SparaOptions-klassen. Varje spara format har en motsvarande klass som innehar spara alternativ för att spara formatet, till exempel det finns ColladaSaveOptions för FileFormat. COLLADA spara format.
###  **Användning av Collada Spara inställningar**
Koden nedan visar hur sparalternativ ska ställas innan en 3D-fil sparas i Collada-format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
###  **Användning av Discreet3DS Spara inställningar**
Koden nedan visar hur man ställer in sparalternativ innan en 3D fil sparas till ett Discreet 3DS-format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
###  **Användning av FBX Spara inställningarna**
Koden nedan visar hur sparalternativ ska ställas innan en 3D-fil sparas till ett FBX-format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
###  **Användning av OBJ Spara inställningar**
Koden nedan visar hur sparalternativ ska anges innan en 3D fil sparas till ett Obj-format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
###  **Användning av STL Spara inställningar**
Koden nedan visar hur man ställer in sparalternativ innan en 3D-fil sparas till STL-format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
###  **Användning av U3D Spara inställningarna**
Koden nedan visar hur sparalternativ ska anges innan ett dokument sparas till U3D format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
###  **Användning av glTF Spara inställningarna**
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 



Koden nedan visar hur sparalternativ ska anges innan ett dokument sparas till glTF format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
###  **PrettyPrint i glTF Spara inställningar**
Du kan också använda setPrettyPrint metod för GLTFSaveOptions klass för människans förståelig JSON-utskrift. Koden nedan visar hur denna funktionalitet används.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
###  **Spara beroenden för en 3D i det verkliga filsystemet**
Utvecklare kan behöva spara alla beroenden av 3D i det riktiga filsystemet. De kan definiera sökvägen för en lokal katalog, spara i `MemoryFileSystem`- objektet eller helt enkelt förkasta beroenden. Egenskapen FileSystem läggs till i alla spara alternativklasser.
####  **Kasta sparande av materialfiler**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
####  **Spara beroende i lokalkatalog**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
####  **Spara beroende i MemoryFileSystem Instans**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
###  **Användning av Google Draco (.DRC) Spara inställningar**
Koden nedan visar hur sparalternativ ska ställas innan en 3D-modell sparas till DRC-formatet.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
###  **Användning av RVM Spara inställningar**
Koden nedan visar hur sparalternativ ska ställas innan en 3D-modell sparas till RVM-formatet.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
