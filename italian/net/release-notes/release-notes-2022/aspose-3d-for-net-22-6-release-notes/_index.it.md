---
title: Aspose.3D for .NET 22.6 Note di rilascio
type: docs
weight: 7
url: /it/net/aspose-3d-for-net-22-6-release-notes/
description: Le note di rilascio dello Aspose.3D for .NET 22.6.
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 22.6.

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



### Aggiunto nuovo metodo alla classe `Aspose.ThreeD.FileFormat`

{{< highlight "csharp" >}}

    /**
     * Gets the preferred file format from the file extension name
     * The extension name should starts with a dot('.').
     * @param extensionName 
     */
    public static FileFormat getFormatByExtension(String extensionName)

{{< /highlight >}}

È possibile ottenere un'istanza FileFormat per nome dell'estensione, codice di esempio:

{{< highlight "csharp" >}}

var scene = new Scene(new Box());
var format = FileFormat.getFormatByExtension(".fbx");
//save the scene to memory stream using FileFormat returned by GetFormatByExtension
var stream = new ByteArrayOutputStream();
scene.save(Stream.wrap(stream), format);


{{< /highlight >}}



### Aggiunto nuovo metodo alla classe `Aspose.ThreeD.Scene`

{{< highlight "csharp" >}}
        /// <summary>
        /// Saves the scene to specified path using specified file format.
        /// </summary>
        /// <param name="fileName">File name.</param>
        public void Save(string fileName)
{{< /highlight >}}

Il nuovo metodo consente di salvare la scena in un file 3D senza fornire un formato di file.

Esempio di codice:

{{< highlight "csharp" >}}

var scene = Scene.FromFile("Input.fbx");
scene.Save("Output.usdz);

{{< /highlight >}}


### Aggiunti nuovi metodi alla classe `Aspose.ThreeD.Transform`

{{< highlight "csharp" >}}
        public Transform SetGeometricTranslation(double x, double y, double z)
        public Transform SetGeometricScaling(double sx, double sy, double sz)
        public Transform SetGeometricRotation(double rx, double ry, double rz)
        public Transform SetTranslation(double tx, double ty, double tz)
        public Transform SetScale(double sx, double sy, double sz)
        public Transform SetEulerAngles(double rx, double ry, double rz)
        public Transform SetRotation(double rw, double rx, double ry, double rz)
        public Transform SetPreRotation(double rx, double ry, double rz)
        public Transform SetPostRotation(double rx, double ry, double rz)
{{< /highlight >}}

Questi metodi di supporto sono forniti for Java/Python associazioni, è anche possibile utilizzarli per fornire una trasformazione in stile catena, codice di esempio:


{{< highlight "csharp" >}}
        var scene = new Scene();
        var node = scene.RootNode.CreateChildNode(new Box());
        node.Transform
                .SetTranslation(10, 0, 0)
                .SetScale(20, 1, 1)
        ;
{{< /highlight >}}
