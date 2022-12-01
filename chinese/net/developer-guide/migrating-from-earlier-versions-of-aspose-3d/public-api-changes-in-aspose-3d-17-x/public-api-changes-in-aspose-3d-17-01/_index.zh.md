---
title: Aspose.3D 17.01中的公共API变化
type: docs
weight: 20
url: /zh/net/public-api-changes-in-aspose-3d-17-01/
---
**内容摘要**

- [在Aspose.ThreeD.FileFormat类中添加PLY格式条目](#PublicAPIChangesinAspose.3D17.01-AddsPLYFormatEntryintheAspose.ThreeD.FileFormatClass)
- [导入PLY文件](#PublicAPIChangesinAspose.3D17.01-ImportingPLYFiles)
- [添加Aspose.ThreeD.GlobalTransform类](#PublicAPIChangesinAspose.3D17.01-AddsAspose.ThreeD.GlobalTransformClass)
- [将GlobalTransform属性添加到Aspose.ThreeD.Node类](#PublicAPIChangesinAspose.3D17.01-AddsaGlobalTransformpropertytoAspose.ThreeD.NodeClass)
- [将多边形属性添加到Aspose.ThreeD.Entities.Mesh类](#PublicAPIChangesinAspose.3D17.01-AddsPolygonspropertytoAspose.ThreeD.Entities.MeshClass)
- [加载3D文件并以自定义二进制格式写入网格](#PublicAPIChangesinAspose.3D17.01-Load3DFileandWriteMeshesinCustomBinaryFormat)
- [从Aspose.ThreeD.Formats.IOConfig类中删除CreateStream成员](#PublicAPIChangesinAspose.3D17.01-RemovesCreateStreammemberfromAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

本文档介绍了Aspose.3D API从版本16.12.0到17.1.0的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对Aspose.3D幕后行为的任何变化的描述。

{{% /alert %}} 
### **在Aspose.ThreeD.FileFormat类中添加PLY格式条目**
为了加载目的，我们添加了一个PLY格式条目。
### **导入PLY文件**
使用最新版本 (17.01) 或更高版本，开发人员可以导入PLY文件。添加PLY格式条目以用于加载目的。

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
### **添加Aspose.ThreeD.GlobalTransform类**
GlobalTransform类提供了与Transform完全相同的接口，但它的所有属性都是只读的。它对于全局转换的目的是有用的。
### **将GlobalTransform属性添加到Aspose.ThreeD.Node类**
它允许访问节点的全局转换。这对于将场景转换为用户的自定义文件格式很有用。
### **将多边形属性添加到Aspose.ThreeD.Entities.Mesh类**
它允许获取网格内部的所有多边形，每个多边形都是多边形顶点索引的数组。在此属性之前，我们必须使用foreach语法来枚举效率低下的每个多边形。
### **加载3D文件并以自定义二进制格式写入网格**
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
### **从Aspose.ThreeD.Formats.IOConfig类中删除CreateStream成员**
这在版本16.11.0中被标记为过时，新的接口文件系统在版本16.11.0中引入，提供了更大的可扩展性。

