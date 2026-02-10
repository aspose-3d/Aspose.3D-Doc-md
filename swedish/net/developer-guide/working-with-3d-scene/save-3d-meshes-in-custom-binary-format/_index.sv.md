---
title: Spara 3D i egna binärformat
type: docs
weight: 20
url: /sv/net/save-3d-meshes-in-custom-binary-format/
description: Använder Aspose. 3D for .NET API, utvecklare kan öppna vilken 3D-fil som stöds, och sedan skriva maskor i den anpassade binärfilen.
---
{{% alert color="primary" %}}

Med [Aspose.3D for .NET API](https://products.aspose.com/3d/net/) kan utvecklare öppna vilken 3D-fil som stöds och sedan skriva maskor i binärfilen.

{{% /alert %}}
##  **Ladda 3D Arkiv och skriva meshes i egna binärformatprogrammeringsprov.**
`Accep`t-metoden exponerad av `RootNode`-medlemmen i [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-klassen tillåter att besöka varje subnod. Kodsnippet nedan tillåter att endast konvertera maskor.

{{< highlight "csharp" >}}
// load a 3D file
Scene scene = Scene.FromFile("test.fbx");

/*
* 3D format demonstration is simple
* 
* struct File {
*   MeshBlock blocks[];
* };
*
* struct Vertex {
*   float x;
*   float y;
*   float z;
* };
* 
* struct Triangle {
*   int a;
*   int b;
*   int c;
* };
* 
* struct MeshBlock {
*   int numControlPoints;
*   int numTriangles;
*   Vertex vertices[numControlPoints];
*   Triangle faces[numTriangles];
* };
*/

// open file for writing in binary mode
using (var writer = new BinaryWriter(new FileStream("Save3DMeshesInCustomBinaryFormat_out", FileMode.Create, FileAccess.Write)))
{
    // visit each descent nodes
    scene.RootNode.Accept(delegate(Node node)
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
