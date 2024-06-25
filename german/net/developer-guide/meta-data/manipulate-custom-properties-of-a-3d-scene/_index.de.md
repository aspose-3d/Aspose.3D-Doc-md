---
title: Benutzer definierte Eigenschaften einer 3D-Szene manipulieren
type: docs
weight: 80
url: /de/net/manipulate-custom-properties-of-a-3d-scene/
description: Entwickler können benutzer definierte Eigenschaften von 3D-Objekten hinzufügen, abrufen und entfernen. Remove Property, Get Property, SetProperty-Mitglieder von 3D-Objekten sind eine Reihe von Shorthanded-Methoden zum Bearbeiten angepasster Eigenschaften des Objekts.
---
##  **Hinzufügen, Abrufen und Entfernen von benutzer definierten Eigenschaften eines 3D-Objekts**
Entwickler können benutzer definierte Eigenschaften von 3D-Objekten hinzufügen, abrufen und entfernen. `RemoveProperty`, `GetProperty`, `SetProperty` Mitglieder von 3D Objekten sind eine Reihe von Shorthanded-Methoden, um angepasste Eigenschaften des Objekts zu manipulieren. Dies ist das Code beispiel, um eine benutzer definierte Eigenschaft festzulegen, abzurufen und zu entfernen:

**C#**

{{< highlight "java" >}}

 // initialize a scene 

Scene scene = new Scene();

// create a Box instance

var box = scene.RootNode.CreateChildNode("box", new Box());

// add custom property

box.SetProperty("property-name", "property-value");

box.SetProperty("property-name2", "property-value2");

// get a custom property by name

Property property = (Property)box.GetProperty("property-name");

// remove the custom property by name or property instance

box.RemoveProperty("property-name");

box.RemoveProperty(property);

// save 3D scene

scene.Save("test.fbx", FileFormat.FBX7400ASCII);

scene.Save("test.gltf", new GLTFSaveOptions(FileFormat.GLTF){SaveExtras = true});

scene.Save("test-2.gltf", new GLTFSaveOptions(FileFormat.GLTF2){SaveExtras = true});

{{< /highlight >}}

{{% alert color="primary" %}} 

Um benutzer definierte Eigenschaften in den GLTF-Modellen zu speichern, müssen Sie SaveE-Extras auf true setzen. Der Standardwert der SaveExtras-Eigenschaft ist false.

{{% /alert %}}
