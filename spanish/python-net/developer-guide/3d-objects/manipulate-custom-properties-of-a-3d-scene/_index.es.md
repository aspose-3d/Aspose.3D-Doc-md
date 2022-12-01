---
title: Manipular propiedades personalizadas de una escena 3D
type: docs
weight: 80
url: /es/python-net/manipulate-custom-properties-of-a-3d-scene/
description: Los desarrolladores pueden agregar, recuperar y eliminar las propiedades personalizadas de los objetos 3D. RemoveProperty, GetProperty, SetProperty Los miembros de 3D objetos son un conjunto de métodos cortos para manipular las propiedades personalizadas del objeto.
---
## **Agregar, recuperar y quitar propiedades personalizadas de un objeto 3D**
Los desarrolladores pueden agregar, recuperar y eliminar las propiedades personalizadas de los objetos 3D. `remove_property`, `get_property`, `set_property` Los miembros de 3D objetos son un conjunto de métodos cortos para manipular las propiedades personalizadas del objeto. Este es el ejemplo de código para establecer, recuperar y quitar una propiedad personalizada:

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

Para guardar propiedades personalizadas en los modelos GLTF, debe establecer `save_extras` a `True`. El valor predeterminado de la propiedad `save_extras` es `False`.

{{% /alert %}}
