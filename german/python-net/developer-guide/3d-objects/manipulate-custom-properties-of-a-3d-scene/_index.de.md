---
title: Benutzer definierte Eigenschaften einer 3D-Szene manipulieren
type: docs
weight: 80
url: /de/python-net/manipulate-custom-properties-of-a-3d-scene/
description: Entwickler können benutzer definierte Eigenschaften von 3D-Objekten hinzufügen, abrufen und entfernen. Remove Property, Get Property, SetProperty-Mitglieder von 3D-Objekten sind eine Reihe von Shorthanded-Methoden zum Bearbeiten angepasster Eigenschaften des Objekts.
---
##  **Hinzufügen, Abrufen und Entfernen von benutzer definierten Eigenschaften eines 3D-Objekts**
Entwickler können benutzer definierte Eigenschaften von 3D-Objekten hinzufügen, abrufen und entfernen. `remove_property`, `get_property`, `set_property` Mitglieder von 3D Objekten sind eine Reihe von Shorthanded-Methoden, um angepasste Eigenschaften des Objekts zu manipulieren. Dies ist das Code beispiel, um eine benutzer definierte Eigenschaft festzulegen, abzurufen und zu entfernen:

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

Um benutzer definierte Eigenschaften in den GLTF-Modellen zu speichern, müssen Sie `save_extras` auf `True` festlegen. Der Standardwert der Eigenschaft `save_extras` beträgt `False`.

{{% /alert %}}
