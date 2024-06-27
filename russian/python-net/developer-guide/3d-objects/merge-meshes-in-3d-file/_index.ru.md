---
title: Объединить сетки в файле 3D
type: docs
weight: 90
url: /ru/python-net/merge-meshes-in-3d-file/
description: Разработчики могут объединять несколько ячеек в одну действительную сетку. Они могут преобразовать все сетки сцены 3D, узла или набора узлов в единую сетку. Чтобы достичь этого, в классе Aspose.ThreeD.Entities.PolygonModifier есть три члена MergeMesh.
---
##  **Объединение сетки в единую действительную сетку**
Разработчики могут объединять несколько ячеек в одну действительную сетку. Они могут преобразовать все сетки сцены 3D, узла или набора узлов в единую сетку. Чтобы достичь этого, в классе `aspose.threed.entities.PolygonModifier` есть несколько членов `merge_mesh`.

В приведенном ниже образце кода объединяются все сетки сцены в одной действительной сетке.

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
