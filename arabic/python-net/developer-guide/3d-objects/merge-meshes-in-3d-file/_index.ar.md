---
title: في 3D ملف
type: docs
weight: 90
url: /ar/python-net/merge-meshes-in-3d-file/
description: يمكن opers إيفلين دمج شبكات متعددة في شبكة صالحة واحدة. Tيا قد تحول كل تنسجم من مشهد 3D ، عقدة أو مجموعة من العقد في شبكة واحدة. In من أجل تحقيق ذلك ، هناك ثلاثة أعضاء erergeMsh في فئة Aspose.ThreeD.
---
## **Merge ينسجم في واحد صالح Msh**
يمكن opers إيفلين دمج شبكات متعددة في شبكة صالحة واحدة. Tيا قد تحول كل تنسجم من مشهد 3D ، عقدة أو مجموعة من العقد في شبكة واحدة. من أجل تحقيق ذلك ، هناك العديد من أعضاء `merge_mesh` في فئة `aspose.threed.entities.PolygonModifier`.

Tانه رمز عينة أدناه دمج جميع تنسجم المشهد في شبكة صالحة واحدة.

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
