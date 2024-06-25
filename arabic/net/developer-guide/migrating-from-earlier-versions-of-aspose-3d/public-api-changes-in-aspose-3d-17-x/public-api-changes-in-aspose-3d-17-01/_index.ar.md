---
title: API العام يتغير بـ Aspose.3D 17.01
type: docs
weight: 20
url: /ar/net/public-api-changes-in-aspose-3d-17-01/
---
**Contents Sأوماري**

- [يضيف إدخال تنسيق PLY في فئة Aspose.ThreeD.FileFormat](#PublicAPIChangesinAspose.3D17.01-AddsPLYFormatEntryintheAspose.ThreeD.FileFormatClass)
- [استيراد ملفات PLY](#PublicAPIChangesinAspose.3D17.01-ImportingPLYFiles)
- [تضيف Aspose.ThreeD. Globalتحويل الطبقة](#PublicAPIChangesinAspose.3D17.01-AddsAspose.ThreeD.GlobalTransformClass)
- [تضيف خاصية تحويل عالمي إلى Aspose.ThreeD.Node Class](#PublicAPIChangesinAspose.3D17.01-AddsaGlobalTransformpropertytoAspose.ThreeD.NodeClass)
- [تضيف خاصية المضلعات إلى Aspose.ThreeD. Quanizes. Mesh Class](#PublicAPIChangesinAspose.3D17.01-AddsPolygonspropertytoAspose.ThreeD.Entities.MeshClass)
- [قم بتحميل ملف 3D وكتابة الشبكات بتنسيق ثنائي مخصص](#PublicAPIChangesinAspose.3D17.01-Load3DFileandWriteMeshesinCustomBinaryFormat)
- [يزيل عضو CreateStream من فئة Aspose.ThreeD. Formes. IOConfig](#PublicAPIChangesinAspose.3D17.01-RemovesCreateStreammemberfromAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

يوضح هذا المستند التغييرات إلى Aspose.3D API من الإصدار 16.12.0 إلى 17.1.0 ، والتي قد تهم مطوري الوحدات/التطبيقات. لا يشمل فقط الطرق العامة الجديدة والمحدثة ، ولكن أيضًا وصفًا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
###  **يضيف إدخال تنسيق PLY في فئة Aspose.ThreeD.FileFormat**
أضفنا إدخال تنسيق PLY لأغراض التحميل.
###  **استيراد ملفات PLY**
باستخدام الإصدار الأخير (17.01) أو أعلى ، يمكن للمطورين استيراد ملفات PLY. تمت إضافة إدخال تنسيق PLY لأغراض التحميل.

**C#**

{{< highlight "java" >}}

 // an entry of PLY file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat PLY;

// initialize Scene class object

Scene scene = new Scene();

// initialize an object

PlyLoadOptions loadPLYOpts = new PlyLoadOptions();

// Flip the coordinate system.

loadPLYOpts.FlipCoordinateSystem = true;

// load 3D Ply model

scene.Open( "3DPlyModel.ply", loadPLYOpts);

{{< /highlight >}}
###  **تضيف Aspose.ThreeD. Globalتحويل الطبقة**
The lolobalTفئة ransform يوفر بالضبط نفس الواجهة مثل ranransform ولكن يتم قراءة جميع خصائصه فقط. It مفيد لأغراض التحويل العالمي.
###  **تضيف خاصية تحويل عالمي إلى Aspose.ThreeD.Node Class**
يسمح It بالوصول إلى التحويل العالمي للعقدة. Tله مفيد لتحويل المشهد إلى تنسيق ملف مخصص للمستخدم.
###  **تضيف خاصية المضلعات إلى Aspose.ThreeD. Quanizes. Mesh Class**
It يسمح للحصول على جميع المضلعات داخل الشبكة ، كل المضلع هو مجموعة من مؤشر القشرة المضلع. في هذه الخاصية ، علينا استخدام كل بناء الجملة لتعداد كل المضلع الذي هو غير فعال.
###  **قم بتحميل ملف 3D وكتابة الشبكات بتنسيق ثنائي مخصص**
**C#**

{{< highlight "java" >}}

 string = @"c:\temp\input.stl", output = @"c:\temp\output";

// load a 3D file

Scene scene = new Scene(input);

/*

\* 3D format demonstration is simple

\* 

\* struct File {

\*   MeshBlock blocks[];

\* };

\*

\* struct Vertex {

\*   float x;

\*   float y;

\*   float z;

\* };

\* 

\* struct Triangle {

\*   int a;

\*   int b;

\*   int c;

\* };

\* 

\* struct MeshBlock {

\*   int numControlPoints;

\*   int numTriangles;

\*   Vertex vertices[numControlPoints];

\*   Triangle faces[numTriangles];

\* };

*/

// open file for writing in binary mode

using (var writer = new BinaryWriter(new FileStream(output, FileMode.Create, FileAccess.Write)))

{

    // visit each descent nodes

    scene.RootNode.Accept(delegate (Node node)

    {

        foreach (Entity entity in node.Entities)

        {

            // only convert meshes, lights/camera and other stuff will be ignored

            if (!(entity is IMeshConvertible))

                continue;

            Mesh m = ((IMeshConvertible)entity).ToMesh();

            var controlPoints = m.ControlPoints;

            // triangulate the mesh, so triFaces will only store triangle indices

            int[][] triFaces = PolygonModifier.Triangulate(controlPoints, m.Polygons);

            // gets the global transform matrix

            Matrix4 transform = node.GlobalTransform.TransformMatrix;

            // write number of control points and triangle indices

            writer.Write(controlPoints.Count);

            writer.Write(triFaces.Length);

            // write control points

            for (int i = 0; i < controlPoints.Count; i++)

            {

                // calculate the control points in world space and save them to file

                var cp = transform * controlPoints[i];

                writer.Write((float)cp.x);

                writer.Write((float)cp.y);

                writer.Write((float)cp.z);

            }

            // write triangle indices

            for (int i = 0; i < triFaces.Length; i++)

            {

                writer.Write(triFaces[i][0]);

                writer.Write(triFaces[i][1]);

                writer.Write(triFaces[i][2]);

            }

        }

        return true;

    });

}

{{< /highlight >}}
###  **يزيل عضو CreateStream من فئة Aspose.ThreeD. Formes. IOConfig**
تم وضع علامة على أنه عفا عليها الزمن في الإصدار 16.11.0 ، تم تقديم واجهة جديدة ilileSyالجذعية في الإصدار 16.11.0 الذي يوفر المزيد من التمدد.

