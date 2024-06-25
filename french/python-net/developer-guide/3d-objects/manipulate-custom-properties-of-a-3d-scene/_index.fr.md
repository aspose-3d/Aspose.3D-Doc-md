---
title: Manipuler les propriétés personnalisées d'une scène 3D
type: docs
weight: 80
url: /fr/python-net/manipulate-custom-properties-of-a-3d-scene/
description: Les développeurs peuvent ajouter, récupérer et supprimer des propriétés personnalisées des objets 3D. Les membres RemoveProperty, GetProperty, SetProperty des objets 3D sont un ensemble de méthodes courtes pour manipuler les propriétés personnalisées de l'objet.
---
##  **Ajouter, récupérer et supprimer des propriétés personnalisées d'un objet 3D**
Les développeurs peuvent ajouter, récupérer et supprimer des propriétés personnalisées des objets 3D. Les membres `remove_property`, `get_property`, `set_property` des objets 3D sont un ensemble de méthodes courtes pour manipuler les propriétés personnalisées de l'objet. Voici l'exemple de code pour définir, récupérer et supprimer une propriété personnalisée:

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

Afin d'enregistrer des propriétés personnalisées dans les modèles GLTF, vous devez définir `save_extras` à `True`. La valeur par défaut de la propriété `save_extras` est `False`.

{{% /alert %}}
