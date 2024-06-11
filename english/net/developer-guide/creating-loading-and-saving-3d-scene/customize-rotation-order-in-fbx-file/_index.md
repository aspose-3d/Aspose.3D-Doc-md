---
title: Customize RotationOrder in FBX file
type: docs
weight: 10
url: /net/customize-rotation-order-in-fbx-file
description: Using Aspose.3D for .NET, developers can define customize the native FBX properties such as RotationOrder.
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), Sometimes, developers require fine control over format-specific features, such as changing the `RotationOrder` in the FBX exporter. While there might not be a public API directly exposing this functionality, Aspose.3D for .NET provides ways to achieve such customizations through its flexible architecture.
{{% /alert %}}



Here’s how you can handle this in Aspose.3D:

{{% highlight csharp %}}

var rvm = Scene.FromFile(@"F1234.rvm");
rvm.RootNode.Accept((Node node) =>
{
    node.SetProperty("RotationOrder", 1); //set a custom property, exporter will match this to FBX's property.
    return true; //continue to traverse on other nodes 
});

rvm.Save(@"test.fbx");

{{% /highlight %}}

In this example:

1.   Create a Scene from a RVM file.
1.   Visit all node in the scene.
1.   Set custom property: The SetProperty method is used to set the `RotationOrder` property, demonstrating how internal mechanisms can be leveraged to control format-specific features not directly exposed by the public API.
1.   Save the Scene: The scene is saved with the customized `RotationOrder`.

By using such techniques, Aspose.3D allows developers to fine-tune and control specific features of 3D formats, ensuring that detailed and precise requirements are met in various 3D applications.