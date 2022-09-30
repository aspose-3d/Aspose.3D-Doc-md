---
title: Bir 3D cene cene MManipulate özel özellikleri
type: docs
weight: 80
url: /tr/python-net/manipulate-custom-properties-of-a-3d-scene/
description: Developers, 3D nesnelerinin özel özelliklerini alabilir, alabilir ve kaldırabilir. RemoveProperty, Get. roperty, Set. roperty üyeleri 3D nesneleri, nesnenin özelleştirilmiş özelliklerini işlemek için kısa teslim yöntemlerden oluşan bir kümedir.
---
## **Add, Retrieve ve Remove 3D Object özel özellikleri**
Developers, 3D nesnelerinin özel özelliklerini alabilir, alabilir ve kaldırabilir. `remove_property`, `get_property`, `set_property` 076. 481 nesnelerinin üyeleri, nesnenin özelleştirilmiş özelliklerini işlemek için bir dizi kısa teslim yöntemidir. This, özel bir özelliği ayarlamak, almak ve kaldırmak için kod örneğidir:

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

Özel özellikleri GLTF modellerine kaydetmek için In siparişi, `save_extras` ila `True` olarak ayarlamanız gerekir. To `save_extras` özelliğinin varsayılan değeri 076481 481 'dir.

{{% /alert %}}
