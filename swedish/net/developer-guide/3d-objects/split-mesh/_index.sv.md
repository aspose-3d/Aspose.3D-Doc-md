---
title: Dela mask
type: docs
weight: 100
url: /sv/net/split-mesh/
description: Utvecklare kan behöva dela upp alla maskor på en scen i flera undermaskor per material. SplitMesh metoden kommer inte att dela en mesh på scenen Om den har tilldelats ett enda material. Utvecklare kan nu uppnå detta genom att använda Aspose.3D for .NET API.
---
## **Dela alla masker av en scen per material**
Utvecklare kan behöva dela upp alla maskor på en scen i flera undermaskor per material. SplitMesh metoden kommer inte att dela en mesh på scenen Om den har tilldelats ett enda material. Utvecklare kan nu uppnå detta genom att användare[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum anger den datapolicy som används i mesh splitting algoritm, det stöder två policyer, dela data mellan delar eller varje delmash har sina egna data (endast använda data).

{{% /alert %}}

Kodprovet nedan delar alla maskor i en scen per material. Varje delmaskin har samma direkta data och skiljer sig endast i index.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.cs" >}}
## **Dela ett mask genom att ange materialet**
Aspose.3D for .NET API gör att utvecklare kan dela en mask genom att manuellt specificera materialet. Alternativet med delad mash skapar separata objekt och varje delmask kommer endast att använda ett material.
### **Dela rutan**
Detta hjälpämne skapar en mesh i rutan för att hålla koden omfattande och kort. Utvecklare kan konstruera en mesh manuellt enligt berättelsen i detta hjälpämne:[Skapa en 3D Cube mesh](/3d/sv/net/create-3d-mesh-and-scene/). Dessutom består en låda av 6 plan och varje plan blir en undernät. Kodprovet nedan delar en primitiv mask genom att manuellt specificera materialet.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.cs" >}}
