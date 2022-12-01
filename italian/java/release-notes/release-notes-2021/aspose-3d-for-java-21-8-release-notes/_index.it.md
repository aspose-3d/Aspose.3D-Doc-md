---
title: Aspose.3D for Java 21.8 Note di rilascio
type: docs
weight: 5
url: /it/java/aspose-3d-for-java-21-8-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 21.8.

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

### Aggiunto com.aspose.threed.Watermark ###

A partire da 21.8 è possibile applicare una filigrana cieca a una mesh e la filigrana può esistere anche dopo essere stata esportata in diversi formati.

{{< highlight "java" >}}

    /**
    * Utility to encode/decode blind watermark  to/from a mesh.
    */
    public class Watermark
    {
        /**
        * Encode a text into mesh' blind watermark.
        * @param input Mesh to encode a blind watermark
        * @param text Text to encode to the mesh
        * @param password Password to protect the watermark, it's optional
        */
        public static Mesh encodeWatermark(Mesh input, String text, String password)
            throws IOException

        /**
        * Decode the watermark from a mesh
        * @param input The mesh to extract watermark
        * @param password The password to decrypt the watermark
        * @throws SecurityException The mesh is protected by password, and provided password is incorrect.
        */
        public static String decodeWatermark(Mesh input, String password)

    }

{{< /highlight >}}


Codice di esempio per generare una mesh con filigrana e salvarla nel file PLY:

{{< highlight "java" >}}
    //prepare a mesh for testing
    var mesh = new Torus().toMesh();
    //encode the watermark to the mesh with password protected
    mesh = Watermark.encodeWatermark(mesh, "Powered by Aspose.3D", "password");
    //save it to a file
    var scene = new Scene(mesh);
    scene.save("watermark-mesh.ply", FileFormat.PLY);
{{< /highlight >}}

Codice di esempio per leggere la filigrana da una mesh:

{{< highlight "java" >}}
    //load a mesh instance from a ply file
    var scene = new Scene("watermark-mesh.ply");
    var mesh = (Mesh)scene.getRootNode().getChild(0).getEntity();
    //read the watermark
    var watermark = Watermark.decodeWatermark(mesh, "password");
    System.out.println(watermark);

{{< /highlight >}}