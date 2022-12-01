---
title: Manipular propiedades personalizadas de una escena 3D
type: docs
weight: 80
url: /es/net/manipulate-custom-properties-of-a-3d-scene/
description: Los desarrolladores pueden agregar, recuperar y eliminar las propiedades personalizadas de los objetos 3D. RemoveProperty, GetProperty, SetProperty Los miembros de 3D objetos son un conjunto de métodos cortos para manipular las propiedades personalizadas del objeto.
---
## **Agregar, recuperar y quitar propiedades personalizadas de un objeto 3D**
Los desarrolladores pueden agregar, recuperar y eliminar las propiedades personalizadas de los objetos 3D. `RemoveProperty`, `GetProperty`, `SetProperty` Los miembros de 3D objetos son un conjunto de métodos cortos para manipular las propiedades personalizadas del objeto. Este es el ejemplo de código para establecer, recuperar y quitar una propiedad personalizada:

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

Para guardar las propiedades personalizadas en los modelos GLTF, debe establecer SaveExtras en verdadero. El valor predeterminado de la propiedad SaveExtras es falso.

{{% /alert %}}
