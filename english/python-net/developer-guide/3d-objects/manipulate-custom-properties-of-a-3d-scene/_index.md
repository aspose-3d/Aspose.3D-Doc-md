---
title: Manipulate custom properties of a 3D Scene
type: docs
weight: 80
url: /python-net/manipulate-custom-properties-of-a-3d-scene/
description: Developers can Add, retrieve, and remove custom properties of 3D objects. RemoveProperty, GetProperty, SetProperty members of 3D objects are a set of short-handed methods to manipulate customized properties of the object.
---

## **Add, Retrieve and Remove custom properties of a 3D Object**
Developers can Add, retrieve, and remove custom properties of 3D objects. `remove_property`, `get_property`, `set_property` members of 3D objects are a set of short-handed methods to manipulate customized properties of the object. This is the code example to set, retrieve and remove a custom property:

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

In order to save custom properties into the GLTF models, you need to set `save_extras` to `True`. The default value of `save_extras` property is `False`.

{{% /alert %}}
