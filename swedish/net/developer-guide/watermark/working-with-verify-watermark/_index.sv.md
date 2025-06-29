---
title: Arbete med Verifiera Vattenstämpel
type: docs
weight: 170
url: /sv/net/working-with-verify-watermark/
---

{{% alert color="primary" %}} 

Med Aspose.3D för .NET API kan utvecklare enkelt lägga till blind vattenmärkeverifiering till 3D-filer samtidigt som de sparas i alla stödda utdatafilformat.

{{% /alert %}} 
# **Skapa en 3D-scen**
Först behöver du skapa en 3D-scen från en 3D-fil. Följande kodsnutt visar hur man använder den här funktionen:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithWatermark-Create3DScene.cs" >}}

# **Dekodera vattenmärke**
Aspose.3D för .NET använder metoden `DecodeWatermark` för att bekräfta vattenmärket för 3D-filen efter att lösenordet har fyllts i. Följande kodsnutt visar hur man använder den här funktionen:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithVerifyWatermark-DecodeWatermark.cs" >}}

# **Dokumentbekräftelse**
För det returnerade resultatet, om det returnerade resultatet är null, betyder det att det inte har lagts till något vattenmärke i 3D-dokumentet. Om det returnerar textinformation är det vattenmärket för 3D-filen. Om lösenordet är inmatat felaktigt kommer ett felmeddelande att returneras.