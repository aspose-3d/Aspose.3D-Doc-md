---
title: Ange 3D Filspararalternativ i C#
linktitle: Ange 3D Filspararalternativ
type: docs
weight: 40
url: /sv/net/specify-3d-file-save-options/
description: Det finns flera Scene.Spara metod överbelastningar som accepterar ett SaveOptions objekt. Varje format spara har en motsvarande klass som innehar spara alternativ för det spara formatet.
---
##  **Översikt**

Den här artikeln förklarar hur du kan spara 3D filer i olika format [Efter att ha laddat dem i Sceneobjekt](https://docs.aspose.com/3d/net/specify-3d-file-load-options/) med C#. Genom att ladda och spara kan du utföra antal olika konverteringar, t.ex.

- Konvertera FBX till X i C#
- Konvertera GLTF till OBJ i C#
- Konvertera OBJ till X i C#
- Konvertera STL till OBJ i C#
- Konvertera RVM till 3DS i C#

##  **3D Filspararalternativ**
Det finns flera överbelastningar med [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) som accepterar ett SparaOptions-objekt. Detta bör vara ett föremål för en klass som härrör från klassen `SaveOptions`. Varje format spara har en motsvarande klass som innehåller sparalternativ för det spara formatet, till exempel, det finns `ColladaSaveOptions` för `FileFormat.Collada` spara formatet.
###  **Användning av Collada Spara inställningarna**
C#-koden nedan visar hur sparalternativ ska ställas innan en 3D-fil sparas i Collada-format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
###  **Användning av Discreet3DS Spara inställningarna**
C#-koden nedan visar hur sparalternativ ska ställas innan en 3D-fil sparas i ett diskret 3DS-format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
###  **Användning av FBX Spara inställningarna**
C#-koden nedan visar hur sparalternativ ska anges innan en 3D-fil sparas till ett FBX-format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

`FBXSaveOptions` exponerar också `EnableCompression` egenskap som kan användas för att komprimera större binärdata i FBX-filen. Standardvärdet för den här egenskapen är sant. Nedan förklarar kod snippet hur du kan arbeta med denna egendom medan du sparar en scen.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
###  **Användning av Obj Spara alternativen**
Koden nedan visar hur sparalternativ ska anges innan en 3D fil sparas till ett Obj-format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
###  **Användning av STL Spara inställningarna**
C#-koden nedan visar hur sparalternativ ska ställas innan en 3D-fil sparas i STL-format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
###  **Användning av U3D Spara inställningarna**
C#-koden nedan visar hur sparalternativ ska anges innan ett dokument sparas i U3D-format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
###  **Användning av glTF Spara inställningarna**
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 



C#-koden nedan visar hur sparalternativ ska anges innan ett dokument sparas i glTF-format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
###  **PrettyPrint i glTF Spara inställningar**
Du kan också använda PrettyPrint-egenskapen för GLTFSaveOptions klass för människans förståelig JSON-utskrift. Koden nedan visar hur denna funktionalitet används.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
###  **Spara beroenden för en 3D i det verkliga filsystemet**
Utvecklare kan behöva spara alla 3D-scener i det riktiga filsystemet. De kan definiera sökvägen för en lokal katalog, spara i `MemoryFileSystem`- objektet eller helt enkelt förkasta beroenden. Egenskapen `FileSystem` läggs till i alla spara alternativklasser.
####  **Kasta sparande av materialfiler**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
####  **Spara beroende i lokalkatalog**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
####  **Spara beroende i MemoryFileSystem- objekt**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
###  **Användning av Google Draco (.drc) Spara inställningar**
C#-koden nedan visar hur sparalternativ ska ställas innan en 3D-modell sparas till DRC-format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
###  **Användning av RVM Spara inställningarna**
C#-koden nedan visar hur sparalternativ ska ställas innan en 3D-modell sparas till RVM-format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
