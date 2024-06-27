---
title: Sammanfoga maskor i 3D file
type: docs
weight: 90
url: /sv/python-net/merge-meshes-in-3d-file/
description: Utvecklare kan slå ihop flera maskor till en enda giltig mask. De kan konvertera alla maskor i en 3D-scen, en nod eller en uppsättning noder till ett enda mesh. För att uppnå detta finns det tre MergeMesh medlemmar i Aspose. 3D. Enheter. PolygonModifier- klass.
---
##  **Sammanfoga maskor till en enda giltig mesh**
Utvecklare kan slå ihop flera maskor till en enda giltig mask. De kan konvertera alla maskor i en 3D-scen, en nod eller en uppsättning noder till ett enda mesh. För att uppnå detta finns det flera `merge_mesh` medlemmar i `aspose.threed.entities.PolygonModifier` klassen.

Kodprovet nedan sammanfogar alla maskor i en scen i ett enda giltigt maskor.

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
