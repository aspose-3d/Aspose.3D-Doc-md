+++
title = "Public API Changes in Aspose.3D 1.2.0" 
description = "" 
weight = 20089 
+++

Aspose.3D for .NET : Public API Changes in Aspose.3D 1.2.0  

# Aspose.3D for .NET : Public API Changes in Aspose.3D 1.2.0


{{< panel title="Contents Summary" style="primary" >}}
*   [Setup the Target and Camera in 3D File](#PublicAPIChangesinAspose.3D1.2.0-SetuptheTargetandCamerain3DFile)
*   [Flip Coordinate System in 3D Formats](#PublicAPIChangesinAspose.3D1.2.0-FlipCoordinateSystemin3DFormats)
*   [How to Triangulate a Mesh](#PublicAPIChangesinAspose.3D1.2.0-HowtoTriangulateaMesh)
{{< /panel >}}
This document describes changes to the Aspose.3D API from version 1.1.0 to 1.2.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

### Setup the Target and Camera in 3D File

In some file formats, light/camera supports target, which allows the light/camera always facing a specified node, this is useful in animation. Example code:

**C#**

{{< code lang="c#" >}}
Scene scene = new Scene();
Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());
cameraNode.Transform.Translation = new Vector3(100, 20, 0);
cameraNode.GetEntity().Target = scene.RootNode.CreateChildNode("target");
scene.Save("d:\\camera-test.3ds", FileFormat.Discreet3DS);
{{< /code >}}

Error rendering macro 'code' : Invalid value specified for parameter lang

### Flip Coordinate System in 3D Formats

(THREEDNET-123) - Allow user to flip coordinate system in OBJ/3DS/STL. Example code:

**C#**

{{< code lang="c#" >}}
Scene scene = new Scene();
scene.Open(@"d:\freehand_shuttle.3ds", new Discreet3DSConfig() {  FlipCoordinateSystem = true });
scene.Save(@"d:\freehand_shuttle.obj", new ObjConfig() { EnableMaterials = false });
{{< /code >}}

Error rendering macro 'code' : Invalid value specified for parameter lang

### How to Triangulate a Mesh

Triangulate mesh is useful for game industry because the triangular is the only supported primitive that GPU hardware supports(non-triangular data are triangulated in driver-level, which is inefficient in real-time rendering). Example code:

**C#**

{{< code lang="c#" >}}
Scene scene = new Scene();
 scene.Open(@"d:\\cube.fbx");
 scene.RootNode.Accept(delegate (Node node)
 {
   Mesh mesh = node.GetEntity<Mesh>();
        if (mesh != null)
        {
            //triangulate the mesh
            Mesh newMesh = PolygonModifier.Triangulate(mesh);
            //replace the old mesh
            node.Entity = mesh;
        }
   return true;
  });
 scene.Save(@"d:\cube-tri.fbx", FileFormat.FBX7400ASCII);
{{< /code >}}

Error rendering macro 'code' : Invalid value specified for parameter lang

