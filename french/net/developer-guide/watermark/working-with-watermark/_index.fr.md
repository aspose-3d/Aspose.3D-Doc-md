---
title: Travailler avec les filigranes
type: docs
weight: 160
url: /fr/net/working-with-watermark/
---

{{% alert color="primary" %}}

En utilisant l'API Aspose.3D pour .NET, les développeurs peuvent facilement ajouter des filigranes aveugles aux fichiers 3D tout en enregistrant dans n'importe quel format de fichier de sortie pris en charge.

{{% /alert %}}
# **Créer une scène 3D**
Vous devez d'abord créer une scène 3D à partir d'un fichier 3D. Le code suivant montre comment utiliser cette fonctionnalité :

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **Encoder le filigrane**
Aspose.3D pour .NET ajoute des informations de texte de filigrane et un mot de passe de filigrane aux fichiers 3D via la méthode ``EncodeWatermark``. Le code suivant montre comment utiliser cette fonctionnalité :

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

# **Enregistrer le document**
Vous pouvez enregistrer dans n'importe quel format de fichier 3D souhaité. Le code suivant montre comment utiliser cette fonctionnalité :

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string output = "output.fbx";
scene.Save(output, FileFormat.FBX7400ASCII);
{{< /highlight >}}