---
title: Aspose.3D for Java 21,8 Utgivning
type: docs
weight: 5
url: /sv/java/aspose-3d-for-java-21-8-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 21.8.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-922 |Lägg till stöd för blind vattenmärke|Ny funktion|
|THREEDNET-920 |Spara till GLB fil med extern draco-kodare förlorade många information.|Felrättning|
|THREEDNET-918 |Signifikant låsning i parallellt Scene.Öppna med fbx-filer|Förbättring|
|THREEDNET-924 |Vertex-avdraget fungerade inte alltid i TriMesh|Felrättning|
|THREEDNET-923 |Ogenomskinlighet hanteras inte i FBX importör|Felrättning|
|THREEDNET-912 |FBX till GLTF2|Felrättning|


## API ändringar ##

### Tillagd com.aspose.3.Vattemärke ###

Från 21.8 kan du applicera en blind vattenstämpel på en Mesh, och vattenmärket kan existera även efter att den har exporterats i olika format.

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


Provkod för att generera en mesh med vattenstämpel och spara den till PLY fil:

{{< highlight "java" >}}
    //prepare a mesh for testing
    var mesh = new Torus().toMesh();
    //encode the watermark to the mesh with password protected
    mesh = Watermark.encodeWatermark(mesh, "Powered by Aspose.3D", "password");
    //save it to a file
    var scene = new Scene(mesh);
    scene.save("watermark-mesh.ply", FileFormat.PLY);
{{< /highlight >}}

Provkod för att avläsa vattenmärket från en mask:

{{< highlight "java" >}}
    //load a mesh instance from a ply file
    var scene = new Scene("watermark-mesh.ply");
    var mesh = (Mesh)scene.getRootNode().getChild(0).getEntity();
    //read the watermark
    var watermark = Watermark.decodeWatermark(mesh, "password");
    System.out.println(watermark);

{{< /highlight >}}