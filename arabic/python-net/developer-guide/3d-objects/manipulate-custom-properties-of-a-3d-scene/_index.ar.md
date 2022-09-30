---
title: Mخصائص مخصصة من 3D cenسين
type: docs
weight: 80
url: /ar/python-net/manipulate-custom-properties-of-a-3d-scene/
description: Dإيفلين يمكن أن Add ، واسترداد ، وإزالة خصائص مخصصة من 3D الكائنات. RemoveProperty ، GetProperty ، أعضاء etProperty من 3D الكائنات هي مجموعة من طرق قصيرة اليد لمعالجة خصائص مخصصة للكائن.
---
## **Add ، Retrieve و ememove خصائص مخصصة من 3D O**
Dإيفلين يمكن أن Add ، واسترداد ، وإزالة خصائص مخصصة من 3D الكائنات. `remove_property`, `get_property`, `set_property` أعضاء 3D الكائنات هي مجموعة من أساليب قصيرة اليد لمعالجة خصائص مخصصة للكائن. Tهو مثال التعليمات البرمجية لتعيين واسترداد وإزالة خاصية مخصصة:

**Python**

```py

# initialize a scene 

from aspose.threed import Scene
from aspose.threed.entities import Box
from aspose.threed.formats import GLTFSaveOptions, FileFormat

scene = Scene()

# create a Box instance

box = scene.root_node.create_child_node("box", Box())

# add custom property

box.set_property("property-name", "property-value");

box.set_property("property-name2", "property-value2");

# get a custom property by name

property = box.get_property("property-name");

# remove the custom property by name or property instance

box.remove_property("property-name");

box.remove_property(property);

# save 3D scene

opt = GLTFSaveOptions(FileFormat.GLTF2)
opt.save_extras = True

scene.save("test-2.gltf", opt)

```

{{% alert color="primary" %}} 

In الطلب لحفظ خصائص مخصصة في نماذج GLTF ، تحتاج إلى تعيين `save_extras` إلى `True`. Tالقيمة الافتراضية `save_extras` الملكية هي `False`.

{{% /alert %}}
