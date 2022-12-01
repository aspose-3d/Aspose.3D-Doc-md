---
title: Aspose.3D per Python via .NET 22,6 Note di rilascio
type: docs
weight: 7
url: /it/python-net/aspose-3d-for-python-net-22-6-release-notes/
description: Le note di rilascio dello Aspose.3D per Python via .NET 22.6.
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D per lo Python via .NET 22.6.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-1152 |Consenti salvare la scena 3D senza specificare il formato del file|Nuova funzione|
|THREEDNET-1157 |SdfValueBlock non è supportato nell'importazione USDZ|Miglioramento|
|THREEDNET-1156 |Eccezione GLF: Impossibile importare glTF, byteOffset non è definito nell'accessorio|Correzione di bug|
|THREEDNET-1154 |Aspose.ThreeD. ExportExportException: Spec duplicata mentre conversione da DAE a USDZ|Correzione di bug|
|THREEDNET-1153 |L'eccezione si verifica durante il risparmio da USDZ a GLTF|Correzione di bug|



## API modifiche ##

### Aggiunto nuovo metodo alla classe `aspose.threed.FileFormat`

{{< highlight "python" >}}
    
    # Gets the preferred file format from the file extension name
    # The extension name should starts with a dot('.').
    def get_format_by_extension(extensionName)

{{< /highlight >}}

È possibile ottenere un'istanza FileFormat per nome dell'estensione, codice di esempio:

{{< highlight "python" >}}

scene = Scene(Box())
format = FileFormat.get_format_by_extension(".fbx")
# save the scene to memory stream using FileFormat returned by GetFormatByExtension
stream = BytesIO()
scene.save(stream, format)

{{< /highlight >}}



### Aggiunto nuovo metodo alla classe `aspose.threed.Scene`

{{< highlight "python" >}}

    # Saves the scene to specified path using specified file format.
    def save(fileName)

{{< /highlight >}}

Il nuovo metodo consente di salvare la scena in un file 3D senza fornire un formato di file.

Esempio di codice:

{{< highlight "python" >}}

scene = Scene.from_file("Input.fbx")
scene.save("Output.usdz)

{{< /highlight >}}
