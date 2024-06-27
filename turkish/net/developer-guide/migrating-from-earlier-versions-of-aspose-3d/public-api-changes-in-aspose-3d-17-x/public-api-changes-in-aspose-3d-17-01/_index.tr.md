---
title: Kamu API Aspose içinde değişir. 3D 17.01
type: docs
weight: 20
url: /tr/net/public-api-changes-in-aspose-3d-17-01/
---
**Contents Summary**

- [Adds PLY Format Entry in the Aspose.ThreeD.FileFormat Class](#PublicAPIChangesinAspose.3D17.01-AddsPLYFormatEntryintheAspose.ThreeD.FileFormatClass)
- [PLY dosyalarını içe aktarma](#PublicAPIChangesinAspose.3D17.01-ImportingPLYFiles)
- [Adds Aspose.ThreeD.GlobalTransform Class](#PublicAPIChangesinAspose.3D17.01-AddsAspose.ThreeD.GlobalTransformClass)
- [Globaltransform özelliğini Aspose 'a ekler. threed. node sınıfı](#PublicAPIChangesinAspose.3D17.01-AddsaGlobalTransformpropertytoAspose.ThreeD.NodeClass)
- [Adds Polygons property to Aspose.ThreeD.Entities.Mesh Class](#PublicAPIChangesinAspose.3D17.01-AddsPolygonspropertytoAspose.ThreeD.Entities.MeshClass)
- [3D dosyasını yükleyin ve özel ikili formatta kafesler yazın](#PublicAPIChangesinAspose.3D17.01-Load3DFileandWriteMeshesinCustomBinaryFormat)
- [Removes CreateStream member from Aspose.ThreeD.Formats.IOConfig Class](#PublicAPIChangesinAspose.3D17.01-RemovesCreateStreammemberfromAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 16.12.0 to 17.1.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Adds PLY Format Entry in the Aspose.ThreeD.FileFormat Class**
Yükleme amacıyla PLY format girişi ekledik.
###  **PLY dosyalarını içe aktarma**
Using the recent version (17.01) or higher, developers can import PLY files. The PLY format entry is added for loading purposes.

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
###  **Adds Aspose.ThreeD.GlobalTransform Class**
He he GlobalTransform sınıfı, Transform gibi tam olarak aynı arayüzü sağlar, ancak tüm özellikleri okunur. It küresel dönüşüm amaçları için yararlıdır.
###  **Globaltransform özelliğini Aspose 'a ekler. threed. node sınıfı**
It, düğümün küresel dönüşümüne erişime izin verir. This, sahneyi kullanıcının özel dosya formatına dönüştürmek için yararlıdır.
###  **Adds Polygons property to Aspose.ThreeD.Entities.Mesh Class**
It, ağın içindeki tüm poligonları almasına izin verir, her çokgen poligon bir dizi poligon vertex indeksidir. Bbu özellik için, verimsiz olan her poligonu numaralandırmak için foreach sözdizimini kullanmalıyız.
###  **3D dosyasını yükleyin ve özel ikili formatta kafesler yazın**
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
###  **Removes CreateStream member from Aspose.ThreeD.Formats.IOConfig Class**
This 16.11.0 sürümünde eski olarak işaretlendi, yeni arayüz 16.ile. ystem 16.11.0 sürümünde daha fazla genişletilebilirlik sağlayan tanıtıldı.

