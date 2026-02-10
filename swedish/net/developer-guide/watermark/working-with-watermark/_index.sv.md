---
title: Arbete med vattenstämpel
type: docs
weight: 160
url: /sv/net/working-with-watermark/
---

{{% alert color="primary" %}} 

Med Aspose.3D för .NET API kan utvecklare enkelt lägga till vattenmärken till 3D-filer samtidigt som de sparas i alla stödda utdatafilformat.

{{% /alert %}} 
# **Skapa en 3D-scen**
Först behöver du skapa en 3D-scen från en 3D-fil. Följande kodsnutt visar hur man använder den här funktionen:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **Koda vattenmärke**
Aspose.3D för .NET lägger till vattenmärksinformation och vattenmärkspassord till 3D-filer via ``EncodeWatermark``-metoden. Följande kodsnutt visar hur man använder den här funktionen:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var numMeshes = 0;
scene.RootNode.Accept((Node node) =>
{
    var mesh = node.GetEntity<Mesh>();
    if (mesh != null)
    {
        numMeshes++;
        mesh = Watermark.EncodeWatermark(mesh, "HelloWorld", "1234");
        if (mesh != null)
        {
            node.Entity = mesh;
        }
    }
    return true;
});
{{< /highlight >}}

# **Spara dokument**
Du kan spara till vilket 3D-filformat du vill. Följande kodsnutt visar hur man använder den här funktionen:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string output = "output.fbx";
scene.Save(output, FileFormat.FBX7400ASCII);
{{< /highlight >}}