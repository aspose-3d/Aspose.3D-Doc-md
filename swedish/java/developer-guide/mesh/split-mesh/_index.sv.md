---
title: Dela mask
type: docs
weight: 10
url: /sv/java/split-mesh/
description: Aspose.3D for Java API har stöd för att dela alla maskor på en scen i flera undermaskor per material. SplitMesh-metoden kommer inte att dela en mesh på scenen, om den har tilldelats ett enda material. Det kan uppnås med hjälp av Aspose.3D for Java API.
---
## **Dela alla masker av Scen per material.**
Aspose.3D for Java API har stöd för att dela alla maskor på en scen i flera undermaskor per material. SplitMesh-metoden kommer inte att dela en mesh på scenen, om den har tilldelats ett enda material. Det kan uppnås med hjälp av Aspose.3D for Java API.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum anger den datapolicy som används i mesh splitting algoritm, det stöder två policyer, dela data mellan delar eller varje delmash har sina egna data (endast använda data).

{{% /alert %}} 

Kodprovet nedan delar alla maskor i en scen per material. Varje delmaskin har samma direkta data och skiljer sig endast i index.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitAllMeshesofScenebyMaterial.java" >}}
## **Dela ett mask genom att ange materialet**
Aspose.3D for Java API har stöd för att dela en mask genom att manuellt specificera materialet. Alternativet med delad mash skapar separata objekt och varje delmask kommer endast att använda ett material.
### **Dela rutan**
Detta hjälpämne skapar en mesh i rutan för att hålla koden omfattande och kort. Utvecklare kan konstruera en mesh manuellt enligt berättelsen i detta hjälpämne:[Skapa en 3D Cube mesh](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Dessutom består en låda av 6 plan och varje plan blir en undernät. Kodprovet nedan delar en primitiv mask genom att manuellt specificera material.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitMeshbyMaterial.java" >}}
