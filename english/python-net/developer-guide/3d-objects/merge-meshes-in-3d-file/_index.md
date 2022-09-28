---
title: Merge Meshes in 3D file
type: docs
weight: 90
url: /python-net/merge-meshes-in-3d-file/
description: Developers can merge multiple meshes into a single valid mesh. They might convert all meshes of a 3D scene, a node or a set of nodes into a single mesh. In order to achieve this, there are three MergeMesh members in the Aspose.ThreeD.Entities.PolygonModifier class.
---

## **Merge Meshes into a single valid Mesh**
Developers can merge multiple meshes into a single valid mesh. They might convert all meshes of a 3D scene, a node or a set of nodes into a single mesh. In order to achieve this, there are three MergeMesh members in the Aspose.ThreeD.Entities.PolygonModifier class.

The code sample below merge all meshes of a scene in a single valid mesh.

**Python**

```py

import aspose.threed as a3d
# load a 3D scene

scene = a3d.Scene.from_file("LAD-TOP.rvm")

# merge all meshes

mesh = a3d.PolygonModifier.merge_mesh(scene)

# encode this mesh into the PLY format

a3d.FileFormat.PLY.encode_mesh(mesh, "LAD-TOP.ply")

```
