---
title: 合并3D文件中的网格
type: docs
weight: 90
url: /zh/python-net/merge-meshes-in-3d-file/
description: 开发人员可以将多个网格合并为一个有效网格。它们可以将3D场景、节点或一组节点的所有网格转换为单个网格。为了实现这一点，在Aspose.ThreeD.Entities.PolygonModifier类中有三个MergeMesh成员。
---
## **将网格合并为单个有效网格**
开发人员可以将多个网格合并为一个有效网格。它们可以将3D场景、节点或一组节点的所有网格转换为单个网格。为了实现这一点，`aspose.threed.entities.PolygonModifier`类中有几个`merge_mesh`成员。

下面的代码示例将场景的所有网格合并到单个有效网格中。

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
