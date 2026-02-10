---
title: Risparmia 3D mesh in formato binario personalizzato
type: docs
weight: 20
url: /it/net/save-3d-meshes-in-custom-binary-format/
description: Utilizzando Aspose.3D for .NET API, gli sviluppatori possono aprire qualsiasi file 3D supportato e quindi scrivere mesh nel file binario personalizzato.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET API](https://products.aspose.com/3d/net/), gli sviluppatori possono aprire qualsiasi file 3D supportato e quindi scrivere mesh nel file binario.

{{% /alert %}}
##  **Carica 3D file e scrivi mesh in formato binario personalizzato campione di programmazione**
Il metodo `Accep`t esposto dal membro `RootNode` nella classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) consente di visitare ogni sub nodo. Lo snippet di codice di seguito consente di convertire solo le mesh.

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
