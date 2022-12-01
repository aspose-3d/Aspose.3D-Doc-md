---
title: Aspose.3D for Java 21.8 tes elease ootes
type: docs
weight: 5
url: /ar/java/aspose-3d-for-java-21-8-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 21.8.

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

### Added com.aspose.threed. ateratermark ###

Rom rom 21.8 يمكنك تطبيق علامة مائية أعمى على esh esh ، ويمكن أن توجد العلامة المائية حتى بعد تصديرها إلى أشكال مختلفة.

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


Sرمز وافرة لتوليد شبكة مع علامة مائية وحفظه إلى PLY الملف:

{{< highlight "java" >}}
    //prepare a mesh for testing
    var mesh = new Torus().toMesh();
    //encode the watermark to the mesh with password protected
    mesh = Watermark.encodeWatermark(mesh, "Powered by Aspose.3D", "password");
    //save it to a file
    var scene = new Scene(mesh);
    scene.save("watermark-mesh.ply", FileFormat.PLY);
{{< /highlight >}}

Sرمز وافرة لقراءة العلامة المائية من شبكة:

{{< highlight "java" >}}
    //load a mesh instance from a ply file
    var scene = new Scene("watermark-mesh.ply");
    var mesh = (Mesh)scene.getRootNode().getChild(0).getEntity();
    //read the watermark
    var watermark = Watermark.decodeWatermark(mesh, "password");
    System.out.println(watermark);

{{< /highlight >}}