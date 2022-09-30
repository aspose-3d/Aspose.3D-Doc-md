---
title: Ange 3D Arkiv Spara inställningar
type: docs
weight: 10
url: /sv/java/specify-3d-file-save-options/
description: Det finns flera Scene.save metod överbelastningar som accepterar en SaveOptions instans.
---
## **3D Arkiv Spara inställningar**
Det finns flera Scene.save metod överbelastningar som accepterar en SaveOptions instans. Detta bör vara en instans av en klass som härrör från SparaOptions-klassen. Varje spara format har en motsvarande klass som innehar spara alternativ för att spara formatet, till exempel det finns ColladaSaveOptions för FileFormat. COLLADA spara format.
### **Användning av Collada Spara alternativa**
Koden nedan visar hur man ställer in spara alternativ innan man sparar en 3D fil i Collada format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
### **Användning av Discreet3DS Spara alternativa**
Koden nedan visar hur man ställer in sparalternativ innan man sparar en 3D fil till ett diskret 3DS format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
### **Användning av FBX Spara alternativa**
Koden nedan visar hur man ställer in spara alternativ innan man sparar en 3D fil till ett FBX format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
### **Användning av OBJ Spara alternativa**
Koden nedan visar hur man ställer in spara alternativ innan man sparar en 3D fil till ett Obj-format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
### **Användning av STL Spara alternativa**
Koden nedan visar hur man ställer in spara alternativ innan man sparar en 3D fil till STL format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
### **Användning av U3D Spara alternativa**
Koden nedan visar hur man ställer in spara alternativ innan man sparar ett dokument till U3D format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
### **Användning av glTF Spara alternativa**
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 



Koden nedan visar hur man ställer in spara alternativ innan man sparar ett dokument till glTF format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
### **PrettyPrint i glTF Spara inställningar**
Du kan också använda setPrettyPrint metod för GLTFSaveOptions klass för människans förståelig JSON-utskrift. Koden nedan visar hur denna funktionalitet används.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
### **Spara beroende på en 3D scen i det verkliga filsystemet**
Utvecklare kan behöva spara alla beroenden av 3D scen i det riktiga filsystemet. De kan definiera sökvägen för en lokal katalog, spara i objektet `MemoryFileSystem` eller helt enkelt förkasta beroenden. Egenskapen FileSystem läggs till i alla spara alternativklasser.
#### **Kasta sparande av materialfiler**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
#### **Spara beroende i lokalkatalog**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
#### **Spara beroende i MemoryFileSystem Instans**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
### **Användning av Google Draco (.DRC) Spara alternativ.**
Koden nedan visar hur man ställer in sparalternativ innan man sparar en 3D modell till DRC format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
### **Användning av RVM Spara alternativa**
Koden nedan visar hur man ställer in sparalternativ innan man sparar en 3D modell till RVM format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
