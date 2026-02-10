---
title: Create 3D Mesh and Scene
type: docs
weight: 10
url: /python-net/create-3d-mesh-and-scene/
description: A Mesh is defined by a set of control points and the many n-sided polygons as needed. This article explains how to define a Mesh.
---

## **Create a 3D Cube Mesh**
A [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) is defined by a set of control points and the many n-sided polygons as needed. This article explains how to define a Mesh.

In order to create a Mesh surface, we need to define control points and polygons as follows:

- [Define the Control Points](/3d/python-net/create-3d-mesh-and-scene/)
- [Create Polygons with PolygonBuilder Class](/3d/python-net/create-3d-mesh-and-scene/)
- [Create Polygons](/3d/python-net/create-3d-mesh-and-scene/)

Here’s an example to attach a Phong material to the cube node:
### **Define the Control Points**
A mesh is composed by a set of control points in space, and polygons to describe the mesh surface, to create a mesh, we need to define the control points:

{{% alert color="primary" %}}

The control points of all geometries in Aspose.3D use homogeneous coordinate, so it’s `Vector4` instead of `Vector3` in the example code.

{{% /alert %}}

**Example:**

{{< highlight "python" >}}
from aspose.threed.utilities import Vector4

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize control points
controlPoints = [Vector4(-5.0, 0.0, 5.0, 1.0), Vector4(5.0, 0.0, 5.0, 1.0), Vector4(5.0, 10.0, 5.0, 1.0), Vector4(-5.0, 10.0, 5.0, 1.0), Vector4(-5.0, 0.0, -5.0, 1.0), Vector4(5.0, 0.0, -5.0, 1.0), Vector4(5.0, 10.0, -5.0, 1.0), Vector4(-5.0, 10.0, -5.0, 1.0)]
{{< /highlight >}}


### **Create Polygons**
The control points are not renderable, to make the cube visible, we need to define polygons in each side:

{{< highlight "python" >}}
from aspose.threed.entities import Mesh

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
controlPoints = DefineControlPoints()
#  Initialize mesh object
mesh = Mesh()
#  Add control points to the mesh
mesh.control_points.extend(controlPoints)
#  Create polygons to mesh
#  Front face (Z+)
mesh.create_polygon([0, 1, 2, 3 ])
#  Right side (X+)
mesh.create_polygon([1, 5, 6, 2 ])
#  Back face (Z-)
mesh.create_polygon([5, 4, 7, 6 ])
#  Left side (X-)
mesh.create_polygon([4, 0, 3, 7 ])
#  Bottom face (Y-)
mesh.create_polygon([0, 4, 5, 1 ])
#  Top face (Y+)
mesh.create_polygon([3, 2, 6, 7 ])
{{< /highlight >}}


### **Create Polygons with PolygonBuilder Class**
We can also define polygon by vertices with `PolygonBuilder` class:

{{< highlight "python" >}}
from aspose.threed.entities import Mesh, PolygonBuilder

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
controlPoints = DefineControlPoints()
#  Initialize mesh object
mesh = Mesh()
#  Add control points to the mesh
mesh.control_points.extend(controlPoints)
#  Indices of the vertices per each polygon
indices = [    0, 1, 2, 3,     1, 5, 6, 2,     5, 4, 7, 6,     4, 0, 3, 7,     0, 4, 5, 1,     3, 2, 6, 7 // Top face (Y+)
]
vertexId = 0
builder = PolygonBuilder(mesh)
for face in range(6):
    #  Start defining a new polygon
    builder.begin()
    for v in range(4):
        #  The indice of vertice per each polygon
        builder.add_vertex(indices[vertexId])
        vertexId = vertexId + 1
    #  Finished one polygon
    builder.end()
{{< /highlight >}}

Now it’s finished, to make the mesh visible, we need to prepare a node for it.
## **How to Triangulate a Mesh**
Triangulate mesh is useful for game industry because the triangular is the only supported primitive that GPU hardware supports (non-triangular data are triangulated in driver-level, which is inefficient in real-time rendering)

{{% alert color="primary" %}}

In this version we only triangulated the polygons since it's required by 3ds file exporting, normals/uvs and other vertex elements are lost during this procedure, we can implement this in the future.

{{% /alert %}}

In this example, we triangulate a Mesh by importing FBX file and saved it in FBX format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.py" >}}
## **Create a 3D Cube Scene**
This topic demonstrates how to add Mesh geometry to the 3D scene. The example code places a cube and save 3D scene in the supported file formats.
### **Create a Cube Node**
A node is invisible, but the geometry attached to the node can be rendered.

{{% alert color="primary" %}}

The Mesh class object is being used in the code. We can [create a `Mesh` class object as narrated there](https://docs.aspose.com/3d/python-net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Example**

{{< highlight "python" >}}
from aspose.threed import FileFormat, Node, Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Initialize Node class object
cubeNode = Node("cube")
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
#  Point node to the Mesh geometry
cubeNode.entity = mesh
#  Add Node to a scene
scene.root_node.child_nodes.append(cubeNode)
#  The path to the documents directory.
output = "out"  + "CubeScene.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7400ASCII)
{{< /highlight >}}

{{% alert color="primary" %}}

NOTE: The entities attached to the root node are usually ignored in CAD/CAM softwares, so we need to create a new node to render the geometry.

{{% /alert %}}
