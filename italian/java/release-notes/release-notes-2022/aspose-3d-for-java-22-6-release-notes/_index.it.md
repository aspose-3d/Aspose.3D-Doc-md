---
title: Aspose.3D for Java 22.6 Note di rilascio
type: docs
weight: 7
url: /it/java/aspose-3d-for-java-22-6-release-notes/
description: Le note di rilascio dello Aspose.3D for Java 22.6.
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 22.6.

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

### Aggiunto nuovo metodo alla classe `com.aspose.threed.FileFormat`:

{{< highlight "csharp" >}}
    /**
     * Gets the preferred file format from the file extension name
     * The extension name should starts with a dot('.').
     * @param extensionName 
     */
    public static FileFormat getFormatByExtension(String extensionName)
{{< /highlight >}}

È possibile ottenere un'istanza FileFormat per nome dell'estensione, codice di esempio:

{{< highlight "java" >}}

var scene = new Scene(new Box());
var format = FileFormat.getFormatByExtension(".fbx");
//save the scene to memory stream using FileFormat returned by GetFormatByExtension
var stream = new ByteArrayOutputStream();
scene.save(Stream.wrap(stream), format);

{{< /highlight >}}



### Aggiunto nuovo metodo alla classe `com.aspose.threed.Scene`:

{{< highlight "java" >}}
    /**
     * Saves the scene to specified path using specified file format.
     * @param fileName File name.
     */
    public void save(String fileName)
        throws IOException;

{{< /highlight >}}

Il nuovo metodo consente di salvare la scena in un file 3D senza fornire un formato di file.

Esempio di codice:

{{< highlight "java" >}}

var scene = Scene.fromFile("Input.fbx");
scene.save("Output.usdz);

{{< /highlight >}}
