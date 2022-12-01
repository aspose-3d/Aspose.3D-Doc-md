---
title: Aspose.3D for .NET 21,8 Utgivning
type: docs
weight: 5
url: /sv/net/aspose-3d-for-net-21-8-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 21.8.

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

### Tillagd Aspose.ThreeD.Utiliteter.Vattemärke ###

Från 21.8 kan du applicera en blind vattenstämpel på en Mesh, och vattenmärket kan existera även efter att den har exporterats i olika format.

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


Provkod för att generera en mesh med vattenstämpel och spara den till PLY fil:

{{< highlight "csharp" >}}
    //prepare a mesh for testing
    var mesh = new Torus().ToMesh();
    //encode the watermark to the mesh with password protected
    mesh = Watermark.EncodeWatermark(mesh, "Powered by Aspose.3D", "password");
    //save it to a file
    var scene = new Scene(mesh);
    scene.Save("watermark-mesh.ply", FileFormat.PLY);
{{< /highlight >}}

Provkod för att avläsa vattenmärket från en mask:

{{< highlight "csharp" >}}
    //load a mesh instance from a ply file
    var scene = new Scene("watermark-mesh.ply");
    var mesh = scene.RootNode.ChildNodes[0].GetEntity<Mesh>();
    //read the watermark
    var watermark = Watermark.DecodeWatermark(mesh, "password");
    Console.WriteLine(watermark);
{{< /highlight >}}