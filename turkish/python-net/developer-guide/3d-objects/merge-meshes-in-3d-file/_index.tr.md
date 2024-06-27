---
title: 3D dosyasında mesh'leri birleştirin
type: docs
weight: 90
url: /tr/python-net/merge-meshes-in-3d-file/
description: Developers can merge multiple meshes into a single valid mesh. They might convert all meshes of a 3D scene, a node or a set of nodes into a single mesh. In order to achieve this, there are three MergeMesh members in the Aspose.ThreeD.Entities.PolygonModifier class.
---
##  **Mvalid tek bir geçerli Mesh içine eshes**
Developers can merge multiple meshes into a single valid mesh. They might convert all meshes of a 3D scene, a node or a set of nodes into a single mesh. In order to achieve this, there are several `merge_mesh` members in the `aspose.threed.entities.PolygonModifier` class.

The kod örneği aşağıdaki bir sahnenin tüm meshlerini tek bir geçerli ağ içinde birleştirir.

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
