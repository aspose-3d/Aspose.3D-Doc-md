---
title: Ange 3D Arkiv Spara inställningar
type: docs
weight: 40
url: /sv/python-net/specify-3d-file-save-options/
description: Det finns flera Scene.Spara metod överbelastningar som accepterar ett SaveOptions objekt. Varje format spara har en motsvarande klass som innehar spara alternativ för det spara formatet.
---
## **3D Arkiv Spara inställningar**
Det finns flera metodöverbelastningar [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene) som accepterar ett `SaveOptions` objekt. Detta bör vara föremål för en klass som härrör från klassen `SaveOptions`. Varje sparformat har en motsvarande klass som innehar sparalternativ för att spara formatet, till exempel, Det finns `ColladaSaveOptions` för `FileFormat.Collada` sparformat.
### **Användning av Collada Spara alternativa**
Koden nedan visar hur man ställer in spara alternativ innan man sparar en 3D fil till Collada format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ColladaSaveOption.py" >}}
### **Användning av Discreet3DS Spara alternativa**
Koden nedan visar hur man ställer in sparalternativ innan man sparar en 3D fil till ett diskret 3DS format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.py" >}}
### **Användning av FBX Spara alternativa**
Koden nedan visar hur man ställer in spara alternativ innan man sparar en 3D fil till ett FBX format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-FBXSaveOption.py" >}}

`FBXSaveOptions` exponerar också `enable_compression` fastighet som kan användas för att komprimera stora binärdata i filen FBX .. Standardvärdet för den här egenskapen är sant. Nedan förklarar kod snippet hur du kan arbeta med denna egendom medan du sparar en scen.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-Save3DScene-Compression.py" >}}
### **Användning av Obj Spara alternativen**
Koden nedan visar hur man ställer in spara alternativ innan man sparar en 3D fil till ett Obj-format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ObjSaveOption.py" >}}
### **Användning av STL Spara alternativa**
Koden nedan visar hur man ställer in spara alternativ innan man sparar en 3D fil till STL format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-STLSaveOption.py" >}}
### **Användning av U3D Spara alternativa**
Koden nedan visar hur man ställer in spara alternativ innan man sparar ett dokument till U3D format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-U3DSaveOption.py" >}}
### **Användning av glTF Spara alternativa**
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 



Koden nedan visar hur man ställer in spara alternativ innan man sparar ett dokument till glTF format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-glTFSaveOptions.py" >}}
### **PrettyPrint i glTF Spara inställningar**
Du kan också använda PrettyPrint-egenskapen för GLTFSaveOptions klass för människans förståelig JSON-utskrift. Koden nedan visar hur denna funktionalitet används.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.py" >}}
### **Spara beroende på en 3D scen i det verkliga filsystemet**
Utvecklare kan behöva spara alla 3D sceneberoenden i det riktiga filsystemet. De kan definiera sökvägen för en lokal katalog, spara i MemoryFileSystem-objektet eller helt enkelt förkasta beroenden. Egenskapen FileSystem läggs till i alla spara alternativklasser.
#### **Kasta sparande av materialfiler**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DiscardSavingMaterial.py" >}}
#### **Spara beroende i lokalkatalog**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.py" >}}
#### **Spara beroende i MemoryFileSystem- objekt**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.py" >}}
### **Användning av Google Draco (.drc) Spara alternativa**
Koden nedan visar hur man ställer in sparalternativ innan man sparar en 3D modell till DRC format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DRCSaveOptions.py" >}}
### **Användning av RVM Spara alternativa**
Koden nedan visar hur man ställer in sparalternativ innan man sparar en 3D modell till RVM format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-RVMSaveOptions.py" >}}
