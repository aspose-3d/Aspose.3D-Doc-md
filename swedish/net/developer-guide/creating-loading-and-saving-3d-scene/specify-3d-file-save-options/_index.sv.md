---
title: Ange 3D Arkiv Spara alternativ i C#
linktitle: Ange 3D Arkiv Spara inställningar
type: docs
weight: 40
url: /sv/net/specify-3d-file-save-options/
description: Det finns flera Scene.Spara metod överbelastningar som accepterar ett SaveOptions objekt. Varje format spara har en motsvarande klass som innehar spara alternativ för det spara formatet.
---
## **Översikt**

Den här artikeln förklarar hur du kan spara 3D filer i olika format[Efter att ha laddat dem i Sceneobjekt](https://docs.aspose.com/3d/net/specify-3d-file-load-options/)C#. Genom att ladda och spara kan du utföra antal olika konverteringar, t.ex.

- Konvertera FBX till X i C#
- Konvertera GLTF till OBJ i C#
- Konvertera OBJ till X i C#
- Konvertera STL till OBJ i C#
- Konvertera RVM till 3DS i C#

## **3D Arkiv Spara inställningar**
Det finns flera metodöverbelastningar [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) som accepterar ett SaveOptions objekt. Detta bör vara föremål för en klass som härrör från klassen `SaveOptions`. Varje sparformat har en motsvarande klass som innehar sparalternativ för att spara formatet, till exempel, Det finns `ColladaSaveOptions` för `FileFormat.Collada` sparformat.
### **Användning av Collada Spara alternativa**
Koden C# nedan visar hur man ställer in sparalternativ innan man sparar en 3D fil till Collada format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
### **Användning av Discreet3DS Spara alternativa**
Koden C# nedan visar hur man ställer in sparalternativ innan man sparar en 3D fil till en Diskret 07611 23481 format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
### **Användning av FBX Spara alternativa**
Koden C# nedan visar hur man ställer in sparalternativ innan man sparar en 3D fil till ett format FBX ..

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

`FBXSaveOptions` exponerar också `EnableCompression` fastighet som kan användas för att komprimera stora binärdata i filen FBX .. Standardvärdet för den här egenskapen är sant. Nedan förklarar kod snippet hur du kan arbeta med denna egendom medan du sparar en scen.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
### **Användning av Obj Spara alternativen**
Koden nedan visar hur man ställer in spara alternativ innan man sparar en 3D fil till ett Obj-format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
### **Användning av STL Spara alternativa**
Koden C# nedan visar hur man ställer in sparalternativ innan man sparar en 3D fil till STL format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
### **Användning av U3D Spara alternativa**
Koden C# nedan visar hur man ställer in sparalternativ innan man sparar ett dokument till U3D format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
### **Användning av glTF Spara alternativa**
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 



Koden C# nedan visar hur man ställer in sparalternativ innan man sparar ett dokument till glTF format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
### **PrettyPrint i glTF Spara inställningar**
Du kan också använda PrettyPrint-egenskapen för GLTFSaveOptions klass för människans förståelig JSON-utskrift. Koden nedan visar hur denna funktionalitet används.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
### **Spara beroende på en 3D scen i det verkliga filsystemet**
Utvecklare kan behöva spara alla 3D sceneberoenden i det riktiga filsystemet. De kan definiera sökvägen för en lokal katalog, spara i objektet `MemoryFileSystem` eller helt enkelt förkasta beroenden. Fastigheten `FileSystem` läggs till i alla spara alternativ klasser.
#### **Kasta sparande av materialfiler**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
#### **Spara beroende i lokalkatalog**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
#### **Spara beroende i MemoryFileSystem- objekt**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
### **Användning av Google Draco (.drc) Spara alternativa**
Koden C# nedan visar hur man ställer in sparalternativ innan man sparar en 3D modell till DRC format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
### **Användning av RVM Spara alternativa**
Koden C# nedan visar hur man ställer in sparalternativ innan man sparar en 3D modell till RVM format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
