---
title: Ange 3D Ladda alternativ för filName
type: docs
weight: 10
url: /sv/java/specify-3d-file-load-options/
description: Det finns flera Scene.open metod överbelastningar eller Scene klass konstruktor överbelastningar som accepterar LoadOptions instans.
---
##  **3D Ladda ner filer**
Det finns flera Scene.open metod överbelastningar eller Scene klass konstruktor överbelastningar som accepterar LoadOptions instans. Detta bör vara en instans av en klass som härrör från klassen LoadOptions. Varje belastningsformat har en motsvarande klass som innehåller belastningsalternativ för det belastningsformatet. till exempel finns det ColladaSaveOptions for the FileFormat. COLLADA spara format.
###  **Use of the Discreet 3DS Load Options**
Koden nedan visar hur laddningsalternativ ska ställas innan en diskret 3DS-fil lads in.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSLoadOption.java" >}}
###  **Användning av Obj-lastalternativ**
Koden nedan visar hur laddningsalternativ ska ställas innan du laddar en 3D Obj-fil.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJLoadOption.java" >}}
###  **Användning av laddandealternativ för STLName**
Koden nedan visar hur laddningsalternativ ska ställas innan du laddar en STL-fil.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLLoadOption.java" >}}
###  **Användning av laddandealternativ för U3DName**
Koden nedan visar hur laddningsalternativ ska ställas innan du laddar en U3D-fil.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DLoadOption.java" >}}
###  **Användning av laddandealternativ för glTFName**
Koden nedan visar hur laddningsalternativ ska ställas innan du laddar en glTF-fil.
####  **Vänd V/T texturkoordinat**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFLoadOptions.java" >}}
###  **Användning av Ply-lastalternativ**
Koden nedan visar hur laddningsalternativ ska anges innan du laddar en PLY-modell.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-PLYLoadOption.java" >}}
###  **Användning av DirectX X-lastalternativ**
Koden nedan visar hur man ställer in laddningsalternativ innan man laddar en DirectX-fil.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-XLoadOption.java" >}}
###  **Use FBX Load Options**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-LoadOptions-FBXLoadOptions.java" >}}
