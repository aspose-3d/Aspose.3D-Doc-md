---
title: Aspose.3D for .NET 21.8 tes elease ootes
type: docs
weight: 5
url: /ar/net/aspose-3d-for-net-21-8-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 21.8.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-922 |Add دعم العلامة المائية أعمى|New eature|
|THREEDNET-920 |Save إلى GLB ملف مع مشفر draco الخارجي فقدت العديد من المعلومات.|إصلاح g ug|
|THREEDNET-918 |Contignificant قفل الخلاف في متوازي cencene. Oالقلم مع ملفات fbx|حركة بلا حدود|
|THREEDNET-924 |Vertex خصم لم يكن يعمل دائما في TriMesh|إصلاح g ug|
|THREEDNET-923 |لا يتم التعامل مع pacpacity في FBX المستورد|إصلاح g ug|
|THREEDNET-912 |FBX إلى GLTF2 issues|إصلاح g ug|


## API التغييرات ##

### Added Aspose.ThreeD. ###

Rom rom 21.8 يمكنك تطبيق علامة مائية أعمى على esh esh ، ويمكن أن توجد العلامة المائية حتى بعد تصديرها إلى أشكال مختلفة.

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


Sرمز وافرة لتوليد شبكة مع علامة مائية وحفظه إلى PLY الملف:

{{< highlight "csharp" >}}
    //prepare a mesh for testing
    var mesh = new Torus().ToMesh();
    //encode the watermark to the mesh with password protected
    mesh = Watermark.EncodeWatermark(mesh, "Powered by Aspose.3D", "password");
    //save it to a file
    var scene = new Scene(mesh);
    scene.Save("watermark-mesh.ply", FileFormat.PLY);
{{< /highlight >}}

Sرمز وافرة لقراءة العلامة المائية من شبكة:

{{< highlight "csharp" >}}
    //load a mesh instance from a ply file
    var scene = new Scene("watermark-mesh.ply");
    var mesh = scene.RootNode.ChildNodes[0].GetEntity<Mesh>();
    //read the watermark
    var watermark = Watermark.DecodeWatermark(mesh, "password");
    Console.WriteLine(watermark);
{{< /highlight >}}