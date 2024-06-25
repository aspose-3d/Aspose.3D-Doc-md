---
title: Ange 3D Filspararalternativ
type: docs
weight: 40
url: /sv/python-net/specify-3d-file-save-options/
description: Det finns flera Scene.Spara metod överbelastningar som accepterar ett SaveOptions objekt. Varje format spara har en motsvarande klass som innehar spara alternativ för det spara formatet.
---
##  **3D Filspararalternativ**
Det finns flera överbelastningar av [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene) som accepterar ett `SaveOptions`-objekt. Detta bör vara ett föremål för en klass som härrör från klassen `SaveOptions`. Varje format spara har en motsvarande klass som innehåller spara alternativ för det spara formatet, till exempel, det finns `ColladaSaveOptions` för `FileFormat.Collada` spara formatet.
###  **Användning av Collada Spara inställningarna**
Koden nedan visar hur man ställer in sparalternativ innan en 3D-fil sparas till Collada-format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ColladaSaveOption.py" >}}
###  **Användning av Discreet3DS Spara inställningarna**
Koden nedan visar hur man ställer in sparalternativ innan en 3D fil sparas till ett Discreet 3DS-format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.py" >}}
###  **Användning av FBX Spara inställningarna**
Koden nedan visar hur sparalternativ ska ställas innan en 3D-fil sparas till ett FBX-format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-FBXSaveOption.py" >}}

`FBXSaveOptions` exponerar också `enable_compression` egenskap som kan användas för att komprimera större binärdata i FBX-filen. Standardvärdet för den här egenskapen är sant. Nedan förklarar kod snippet hur du kan arbeta med denna egendom medan du sparar en scen.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-Save3DScene-Compression.py" >}}
###  **Användning av Obj Spara alternativen**
Koden nedan visar hur sparalternativ ska anges innan en 3D fil sparas till ett Obj-format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ObjSaveOption.py" >}}
###  **Användning av STL Spara inställningarna**
Koden nedan visar hur man ställer in sparalternativ innan en 3D-fil sparas till STL-format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-STLSaveOption.py" >}}
###  **Användning av U3D Spara inställningarna**
Koden nedan visar hur sparalternativ ska anges innan ett dokument sparas till U3D format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-U3DSaveOption.py" >}}
###  **Användning av glTF Spara inställningarna**
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 



Koden nedan visar hur sparalternativ ska anges innan ett dokument sparas till glTF format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-glTFSaveOptions.py" >}}
###  **PrettyPrint i glTF Spara inställningar**
Du kan också använda PrettyPrint-egenskapen för GLTFSaveOptions klass för människans förståelig JSON-utskrift. Koden nedan visar hur denna funktionalitet används.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.py" >}}
###  **Spara beroenden för en 3D i det verkliga filsystemet**
Utvecklare kan behöva spara alla 3D-scener i det riktiga filsystemet. De kan definiera sökvägen för en lokal katalog, spara i MemoryFileSystem-objektet eller helt enkelt förkasta beroenden. Egenskapen FileSystem läggs till i alla spara alternativklasser.
####  **Kasta sparande av materialfiler**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DiscardSavingMaterial.py" >}}
####  **Spara beroende i lokalkatalog**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.py" >}}
####  **Spara beroende i MemoryFileSystem- objekt**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.py" >}}
###  **Användning av Google Draco (.drc) Spara inställningar**
Koden nedan visar hur sparalternativ ska ställas innan en 3D-modell sparas till DRC-formatet.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DRCSaveOptions.py" >}}
###  **Användning av RVM Spara inställningarna**
Koden nedan visar hur sparalternativ ska ställas innan en 3D-modell sparas till RVM-formatet.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-RVMSaveOptions.py" >}}
