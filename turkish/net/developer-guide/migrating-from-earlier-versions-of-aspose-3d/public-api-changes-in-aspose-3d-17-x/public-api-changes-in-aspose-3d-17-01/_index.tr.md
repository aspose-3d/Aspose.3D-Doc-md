---
title: Public API Changes Aspose.3D 17.01
type: docs
weight: 20
url: /tr/net/public-api-changes-in-aspose-3d-17-01/
---
**Contents Summary**

- [Dds dds PLY Format try ntry Aspose.ThreeD.FileFormat lass lass](#PublicAPIChangesinAspose.3D17.01-AddsPLYFormatEntryintheAspose.ThreeD.FileFormatClass)
- [07mporting PLY Files](#PublicAPIChangesinAspose.3D17.01-ImportingPLYFiles)
- [Dds dds Aspose.ThreeD.GlobalTransform lass lass](#PublicAPIChangesinAspose.3D17.01-AddsAspose.ThreeD.GlobalTransformClass)
- [Dds dds a GlobalTransform özelliği Aspose.ThreeD.Node lass lass](#PublicAPIChangesinAspose.3D17.01-AddsaGlobalTransformpropertytoAspose.ThreeD.NodeClass)
- [Dds dds olyolygons özelliği Aspose.ThreeD.Entities.Mesh lass lass](#PublicAPIChangesinAspose.3D17.01-AddsPolygonspropertytoAspose.ThreeD.Entities.MeshClass)
- [Load 3D File ve Wushes eshes in uustom Binary Format](#PublicAPIChangesinAspose.3D17.01-Load3DFileandWriteMeshesinCustomBinaryFormat)
- [Removes 07reateStream üyesi Aspose.ThreeD.Formats. Ionononfig lass member](#PublicAPIChangesinAspose.3D17.01-RemovesCreateStreammemberfromAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

Tonun belgesi, 16.12.0 sürümünden 17.1.0 'a kadar Aspose.3D API 'teki değişiklikleri açıklar, bu da modül/uygulama geliştiricilerine ilgi gösterebilir. It sadece yeni ve güncellenmiş kamu yöntemlerini değil, aynı zamanda Aspose.3D 'deki sahnelerin arkasındaki davranıştaki herhangi bir değişikliğin açıklamasını da içerir.

{{% /alert %}} 
### **Dds dds PLY Format try ntry Aspose.ThreeD.FileFormat lass lass**
We yükleme amacıyla PLY formatlı bir giriş ekledi.
### **07mporting PLY Files**
Son sürümü (17.01) veya daha yüksek olan developers sing, geliştiriciler PLY dosyalarını içe aktarabilir. Yükleme amacıyla 07he PLY format girişi eklenir.

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
### **Dds dds Aspose.ThreeD.GlobalTransform lass lass**
He he GlobalTransform sınıfı, Transform gibi tam olarak aynı arayüzü sağlar, ancak tüm özellikleri okunur. It küresel dönüşüm amaçları için yararlıdır.
### **Dds dds a GlobalTransform özelliği Aspose.ThreeD.Node lass lass**
It, düğümün küresel dönüşümüne erişime izin verir. This, sahneyi kullanıcının özel dosya formatına dönüştürmek için yararlıdır.
### **Dds dds olyolygons özelliği Aspose.ThreeD.Entities.Mesh lass lass**
It, ağın içindeki tüm poligonları almasına izin verir, her çokgen poligon bir dizi poligon vertex indeksidir. Bbu özellik için, verimsiz olan her poligonu numaralandırmak için foreach sözdizimini kullanmalıyız.
### **Load 3D File ve Wushes eshes in uustom Binary Format**
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
### **Removes 07reateStream üyesi Aspose.ThreeD.Formats. Ionononfig lass member**
This 16.11.0 sürümünde eski olarak işaretlendi, yeni arayüz 16.ile. ystem 16.11.0 sürümünde daha fazla genişletilebilirlik sağlayan tanıtıldı.

