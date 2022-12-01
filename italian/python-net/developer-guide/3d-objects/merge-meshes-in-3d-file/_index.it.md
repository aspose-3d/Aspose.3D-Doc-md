---
title: Unisci le maglie nel file 3D
type: docs
weight: 90
url: /it/python-net/merge-meshes-in-3d-file/
description: Gli sviluppatori possono unire più mesh in un'unica mesh valida. Potrebbero convertire tutte le mesh di una scena 3D, un nodo o un insieme di nodi in una singola mesh. Per raggiungere questo obiettivo, ci sono tre membri MergeMesh nella classe Aspose.ThreeD.Entities.PolygonModifier.
---
## **Unisci le maglie in un'unica mesh valida**
Gli sviluppatori possono unire più mesh in un'unica mesh valida. Potrebbero convertire tutte le mesh di una scena 3D, un nodo o un insieme di nodi in una singola mesh. Per raggiungere questo obiettivo, ci sono diversi membri `merge_mesh` nella classe `aspose.threed.entities.PolygonModifier`.

Il codice di esempio seguente unisce tutte le mesh di una scena in una singola mesh valida.

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
