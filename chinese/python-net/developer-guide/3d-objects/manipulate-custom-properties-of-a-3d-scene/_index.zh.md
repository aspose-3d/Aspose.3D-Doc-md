---
title: 操作3D场景的自定义属性
type: docs
weight: 80
url: /zh/python-net/manipulate-custom-properties-of-a-3d-scene/
description: 开发人员可以添加、检索和删除3D对象的自定义属性。3D对象的RemoveProperty、GetProperty、SetProperty成员是一组短手方法，用于操作对象的自定义属性。
---
## **添加、检索和删除3D对象的自定义属性**
开发人员可以添加、检索和删除3D对象的自定义属性。`remove_property`，`get_property`，3D对象的`set_property`成员是一组短手方法来操纵对象的定制属性。这是设置，检索和删除自定义属性的代码示例:

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

为了将自定义属性保存到GLTF模型中，您需要将`save_extras`设置为`True`。`save_extras`属性的默认值为`False`。

{{% /alert %}}
