---
title: Arbeiten mit Wasserzeichen
type: docs
weight: 160
url: /de/net/working-with-watermark/
---

{{% alert color="primary" %}} 

Mit der Aspose.3D für .NET API können Entwickler problemlos unsichtbare Wasserzeichen zu 3D-Dateien hinzufügen, während sie in jedem unterstützten Ausgabedateiformat speichern.

{{% /alert %}} 
# **Erstellen einer 3D-Szene**
Zuerst müssen Sie eine 3D-Szene aus einer 3D-Datei erstellen. Der folgende Codeausschnitt zeigt, wie Sie diese Funktionalität verwenden:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **Wasserzeichen kodieren**
Aspose.3D für .NET fügt 3D-Dateien Wasserzeichen-Textinformationen und ein Wasserzeichen-Passwort über die ``EncodeWatermark``-Methode hinzu. Der folgende Codeausschnitt zeigt, wie Sie diese Funktionalität verwenden:

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

# **Dokument speichern**
Sie können in jedem 3D-Dateiformat speichern, das Sie möchten. Der folgende Codeausschnitt zeigt, wie Sie diese Funktionalität verwenden:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string output = "output.fbx";
scene.Save(output, FileFormat.FBX7400ASCII);
{{< /highlight >}}