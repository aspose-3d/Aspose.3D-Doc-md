---
title: Fusionner les maillages dans le fichier 3D
type: docs
weight: 90
url: /fr/python-net/merge-meshes-in-3d-file/
description: Les développeurs peuvent fusionner plusieurs maillages en un seul maillage valide. Ils peuvent convertir tous les maillages d'une scène 3D, d'un nœud ou d'un ensemble de nœuds en un seul maillage. Pour ce faire, il y a trois membres MergeMesh dans la classe Aspose.ThreeD.Entities.PolygonModifier.
---
##  **Fusionner les mailles en un seul maillage valide**
Les développeurs peuvent fusionner plusieurs maillages en un seul maillage valide. Ils peuvent convertir tous les maillages d'une scène 3D, d'un nœud ou d'un ensemble de nœuds en un seul maillage. Pour ce faire, il y a plusieurs membres `merge_mesh` dans la classe `aspose.threed.entities.PolygonModifier`.

L'exemple de code ci-dessous fusionne tous les maillages d'une scène dans un seul maillage valide.

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
