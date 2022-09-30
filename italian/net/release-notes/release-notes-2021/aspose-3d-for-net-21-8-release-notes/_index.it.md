---
title: Aspose.3D for .NET 21.8 Note di rilascio
type: docs
weight: 5
url: /it/net/aspose-3d-for-net-21-8-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 21.8.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-922 |Aggiungi supporto per filigrana cieca|Nuova funzione|
|THREEDNET-920 |Salva a GLB file con encoder draco esterno perso molte informazioni.|Correzione di bug|
|THREEDNET-918 |Lizza di blocco significativa in scena parallelizzata. Apri con file fbx|Miglioramento|
|THREEDNET-924 |La deduzione del vertice non era sempre funzionante in TriMesh|Correzione di bug|
|THREEDNET-923 |L'opacità non è gestita nell'importatore FBX|Correzione di bug|
|THREEDNET-912 |Problemi di conversione da FBX a GLTF2|Correzione di bug|


## API modifiche ##

### Aggiunto Aspose.ThreeD.Utilities.Watermark ###

A partire da 21.8 è possibile applicare una filigrana cieca a una mesh e la filigrana può esistere anche dopo essere stata esportata in diversi formati.

{{< highlight "csharp" >}}

    /// <summary>
    /// Utility to encode/decode blind watermark  to/from a mesh.
    /// </summary>
    public class Watermark
    {
        /// <summary>
        /// Encode a text into mesh' blind watermark.
        /// </summary>
        /// <param name="input">Mesh to encode a blind watermark</param>
        /// <param name="text">Text to encode to the mesh</param>
        /// <param name="password">Password to protect the watermark, it's optional</param>
        /// <returns></returns>
        public static Mesh EncodeWatermark(Mesh input, string text, string password)


        /// <summary>
        /// Decode the watermark from a mesh
        /// </summary>
        /// <param name="input">The mesh to extract watermark</param>
        /// <param name="password">The password to decrypt the watermark</param>
        /// <exception cref="System.UnauthorizedAccessException">The mesh is protected by password, and provided password is incorrect.</exception>
        /// <returns></returns>
        public static string DecodeWatermark(Mesh input, string password)
    }

{{< /highlight >}}


Codice di esempio per generare una mesh con filigrana e salvarla nel file PLY:

{{< highlight "csharp" >}}
    //prepare a mesh for testing
    var mesh = new Torus().ToMesh();
    //encode the watermark to the mesh with password protected
    mesh = Watermark.EncodeWatermark(mesh, "Powered by Aspose.3D", "password");
    //save it to a file
    var scene = new Scene(mesh);
    scene.Save("watermark-mesh.ply", FileFormat.PLY);
{{< /highlight >}}

Codice di esempio per leggere la filigrana da una mesh:

{{< highlight "csharp" >}}
    //load a mesh instance from a ply file
    var scene = new Scene("watermark-mesh.ply");
    var mesh = scene.RootNode.ChildNodes[0].GetEntity<Mesh>();
    //read the watermark
    var watermark = Watermark.DecodeWatermark(mesh, "password");
    Console.WriteLine(watermark);
{{< /highlight >}}