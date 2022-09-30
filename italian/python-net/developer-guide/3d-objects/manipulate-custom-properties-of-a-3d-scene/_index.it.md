---
title: Manipolare le proprietà personalizzate di una scena 3D
type: docs
weight: 80
url: /it/python-net/manipulate-custom-properties-of-a-3d-scene/
description: Gli sviluppatori possono aggiungere, recuperare e rimuovere proprietà personalizzate di 3D oggetti. I membri RemoveProperty, GetProperty, SetProperty di 3D oggetti sono un insieme di metodi a corto raggio per manipolare le proprietà personalizzate dell'oggetto.
---
## **Aggiungere, recuperare e rimuovere le proprietà personalizzate di un oggetto 3D**
Gli sviluppatori possono aggiungere, recuperare e rimuovere proprietà personalizzate di 3D oggetti. `remove_property`, `get_property`, `set_property` i membri di 3D oggetti sono un insieme di metodi a corto raggio per manipolare le proprietà personalizzate dell'oggetto. Questo è l'esempio di codice per impostare, recuperare e rimuovere una proprietà personalizzata:

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

Per salvare le proprietà personalizzate nei modelli GLTF, è necessario impostare da `save_extras` a `True`. Il valore predefinito della proprietà `save_extras` è `False`.

{{% /alert %}}
