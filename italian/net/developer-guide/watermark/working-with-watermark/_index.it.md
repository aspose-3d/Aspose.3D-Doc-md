---
title: Lavorare con il Marchio Filigrana
type: docs
weight: 160
url: /it/net/working-with-watermark/
---

{{% alert color="primary" %}}

Utilizzando l'API Aspose.3D for .NET, gli sviluppatori possono facilmente aggiungere watermark invisibili a file 3D durante il salvataggio in qualsiasi formato di file di output supportato.

{{% /alert %}}
# **Crea una Scena 3D**
Innanzitutto, è necessario creare una scena 3D da un file 3D. Il seguente frammento di codice mostra come utilizzare questa funzionalità:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **Codifica Watermark**
Aspose.3D for .NET aggiunge informazioni sul testo del watermark e la password del watermark ai file 3D tramite il metodo ``EncodeWatermark``. Il seguente frammento di codice mostra come utilizzare questa funzionalità:

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

# **Salva Documento**
È possibile salvare in qualsiasi formato di file 3D desiderato. Il seguente frammento di codice mostra come utilizzare questa funzionalità:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string output = "output.fbx";
scene.Save(output, FileFormat.FBX7400ASCII);
{{< /highlight >}}