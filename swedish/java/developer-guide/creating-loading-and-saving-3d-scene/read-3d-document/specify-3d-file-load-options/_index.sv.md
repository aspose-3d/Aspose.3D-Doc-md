---
title: Ange 3D Filladdningsalternativ
type: docs
weight: 10
url: /sv/java/specify-3d-file-load-options/
description: Det finns flera Scene.open metod överbelastningar eller Scene klass konstruktor överbelastningar som accepterar LoadOptions instans.
---
## **3D Filladdningsalternativ**
Det finns flera Scene.open metod överbelastningar eller Scene klass konstruktor överbelastningar som accepterar LoadOptions instans. Detta bör vara en instans av en klass som härrör från klassen LoadOptions. Varje belastningsformat har en motsvarande klass som innehåller belastningsalternativ för det belastningsformatet. till exempel finns det ColladaSaveOptions for the FileFormat. COLLADA spara format.
### **Användning av diskret 3DS lastalternativ**
Koden nedan visar hur man ställer in lastalternativ innan man laddar en diskret 3DS-fil.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSLoadOption.java" >}}
### **Användning av Obj-lastalternativ**
Koden nedan visar hur man ställer in belastningsalternativ innan man laddar en 3D Obj-fil.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJLoadOption.java" >}}
### **Användning av belastningsalternativ STL**
Koden nedan visar hur man ställer in belastningsalternativ innan man laddar en STL-fil.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLLoadOption.java" >}}
### **Användning av belastningsalternativ U3D**
Koden nedan visar hur man ställer in belastningsalternativ innan man laddar en U3D-fil.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DLoadOption.java" >}}
### **Användning av belastningsalternativ glTF**
Koden nedan visar hur man ställer in belastningsalternativ innan man laddar en glTF-fil.
#### **Vänd V/T texturkoordinat**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFLoadOptions.java" >}}
### **Användning av Ply-lastalternativ**
Koden nedan visar hur man ställer in belastningsalternativ innan man laddar en PLY modell.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-PLYLoadOption.java" >}}
### **Användning av DirectX X-lastalternativ**
Koden nedan visar hur man ställer in belastningsalternativ innan man laddar en DirectX X-fil.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-XLoadOption.java" >}}
### **Använd FBX lastalternativ**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-LoadOptions-FBXLoadOptions.java" >}}
