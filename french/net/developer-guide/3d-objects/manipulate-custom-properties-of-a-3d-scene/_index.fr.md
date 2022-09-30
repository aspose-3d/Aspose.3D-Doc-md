---
title: Manipuler les propriétés personnalisées d'une scène 3D
type: docs
weight: 80
url: /fr/net/manipulate-custom-properties-of-a-3d-scene/
description: Les développeurs peuvent ajouter, récupérer et supprimer des propriétés personnalisées d'objets 3D. RemoveProperty, GetProperty, SetProperty Les membres des objets 3D sont un ensemble de méthodes en désavantage numérique pour manipuler les propriétés personnalisées de l'objet.
---
## **Ajouter, récupérer et supprimer des propriétés personnalisées d'un objet 3D**
Les développeurs peuvent ajouter, récupérer et supprimer des propriétés personnalisées d'objets 3D. `RemoveProperty`, `GetProperty`, `SetProperty` Les membres des objets 3D sont un ensemble de méthodes en désavantage numérique pour manipuler les propriétés personnalisées de l'objet. C'est l'exemple de code pour définir, récupérer et supprimer une propriété personnalisée:

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

Afin d'enregistrer des propriétés personnalisées dans les modèles GLTF, vous devez définir SaveExtras à true. La valeur par défaut de la propriété SaveExtras est false.

{{% /alert %}}
