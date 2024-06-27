---
title: Manipulera egna egenskaper för en 3D Scene
type: docs
weight: 80
url: /sv/python-net/manipulate-custom-properties-of-a-3d-scene/
description: Utvecklare kan lägga till, hämta och ta bort egna egenskaper för 3D objekt. Ta bortProperty, HämtaProperty, SetProperty medlemmar i 3D-objekt är en uppsättning korthända metoder för att manipulera anpassade egenskaper för objektet.
---
##  **Lägg till, hämta och ta bort egna egenskaper för ett 3D Objekt**
Utvecklare kan lägga till, hämta och ta bort egna egenskaper för 3D objekt. `remove_property`, `get_property`, `set_property` medlemmar i 3D objekt är en uppsättning korthända metoder för att manipulera anpassade egenskaper för objektet. Det här är kodexemplet för att ange, hämta och ta bort en egenskap:

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

För att spara egna egenskaper i modellerna GLTF måste du ställa in `save_extras` till `True`. Standardvärdet på egenskapen `save_extras` är `False`.

{{% /alert %}}
