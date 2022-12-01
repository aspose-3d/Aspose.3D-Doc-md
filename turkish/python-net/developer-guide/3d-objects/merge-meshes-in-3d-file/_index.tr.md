---
title: M07M3D dosyasında eshes
type: docs
weight: 90
url: /tr/python-net/merge-meshes-in-3d-file/
description: Developers, birden fazla mesh'i tek bir geçerli ağa birleştirebilir. They, 3D sahnesinin, bir düğümün veya düğümlerin tümünü tek bir ağa dönüştürebilir. In bunu başarmak için, Aspose.ThreeD.Entities. olyolygon. odifier sınıfında üç MergeMesh üyesi vardır.
---
## **Mvalid tek bir geçerli Mesh içine eshes**
Developers, birden fazla mesh'i tek bir geçerli ağa birleştirebilir. They, 3D sahnesinin, bir düğümün veya düğümlerin tümünü tek bir ağa dönüştürebilir. In bunu başarmak için `aspose.threed.entities.PolygonModifier` sınıfında birkaç `merge_mesh` üyesi var.

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
