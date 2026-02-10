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

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **Dekodera vattenmärke**
Aspose.3D för .NET använder metoden `DecodeWatermark` för att bekräfta vattenmärket för 3D-filen efter att lösenordet har fyllts i. Följande kodsnutt visar hur man använder den här funktionen:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string text = null;
try
{
    scene.RootNode.Accept((Node node) =>
    {
        var mesh = node.GetEntity<Mesh>();
        if (mesh != null)
        {
            text = Watermark.DecodeWatermark(mesh, "1234");
            if (text != null)
                return false;
        }
        return true;
    });
}
catch (UnauthorizedAccessException)
{
    return "Password error";
}
return text;
{{< /highlight >}}

# **Dokumentbekräftelse**
För det returnerade resultatet, om det returnerade resultatet är null, betyder det att det inte har lagts till något vattenmärke i 3D-dokumentet. Om det returnerar textinformation är det vattenmärket för 3D-filen. Om lösenordet är inmatat felaktigt kommer ett felmeddelande att returneras.