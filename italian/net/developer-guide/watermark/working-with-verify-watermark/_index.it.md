---
title: Lavorare con Verify Watermark
type: docs
weight: 170
url: /it/net/working-with-verify-watermark/
---

{{% alert color="primary" %}}

Utilizzando l'API Aspose.3D per .NET, gli sviluppatori possono facilmente aggiungere una verifica di filigrana (watermark) ai file 3D durante il salvataggio in qualsiasi formato di file di output supportato.

{{% /alert %}}
# **Crea una Scena 3D**
Innanzitutto, è necessario creare una scena 3D da un file 3D. Il seguente frammento di codice mostra come utilizzare questa funzionalità:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **Decodifica la Filigrana (Watermark)**
Aspose.3D per .NET utilizza il metodo `DecodeWatermark` per confermare la filigrana (watermark) per il file 3D dopo aver inserito la password. Il seguente frammento di codice mostra come utilizzare questa funzionalità:

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

# **Conferma del Documento**
Per il risultato restituito, se il risultato restituito è nullo, significa che non è stata aggiunta alcuna filigrana (watermark) al documento 3D. Se restituisce informazioni di testo, si tratta della filigrana (watermark) del file 3D. Se la password è inserita in modo errato, verrà restituito un messaggio di errore.