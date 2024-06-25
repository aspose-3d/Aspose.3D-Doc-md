---
title: Dela mask
type: docs
weight: 100
url: /sv/python-net/split-mesh/
description: Utvecklare kan behöva dela upp alla maskor på en scen i flera undermaskor per material. SplitMesh metoden kommer inte att dela en mesh på scenen Om den har tilldelats ett enda material. Utvecklare kan nu åstadkomma detta genom att använda Aspose.3D for Python via .NET API.
---
##  **Dela alla masker av en scen per material**
Utvecklare kan behöva dela upp alla maskor på en scen i flera undermaskor per material. `split_mesh`-metoden delar inte en mask på scenen om den har tilldelats ett enda material. Utvecklare kan nu åstadkomma detta genom att använda [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum anger datapolicyn som används i algoritmen för uppdelning av mesh. Den stöder två regler. dela data mellan delar eller varje delmash har sina egna data (endast använda data).

{{% /alert %}}

Kodprovet nedan delar alla maskor i en scen per material. Varje delmaskin har samma direkta data och skiljer sig endast i index.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.py" >}}
##  **Dela ett mask genom att ange materialet**
Aspose.3D for Python via .NET API tillåter utvecklare att dela en mesh genom att manuellt ange materialet. Alternativet med delad mash skapar separata objekt och varje delmask kommer endast att använda ett material.
###  **Dela rutan**
Detta hjälpämne skapar en mesh i rutan för att hålla koden omfattande och kort. Utvecklare kan konstruera en mesh manuellt som är berättad i detta hjälpämne: [Skapa en 3D kubst](/3d/sv/python-net/create-3d-mesh-and-scene/). Dessutom består en låda av 6 plan och varje plan blir en undernät. Kodprovet nedan delar en primitiv mask genom att manuellt specificera materialet.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.py" >}}
