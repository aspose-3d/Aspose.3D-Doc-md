---
title: Personnaliser RotationOrder dans le fichier FBX
type: docs
weight: 10
url: /fr/net/customize-rotation-order-in-fbx-file
description: En utilisant Aspose.3D for .NET, les développeurs peuvent définir les propriétés natives FBX telles que RotationOrder.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/), parfois, les développeurs exigent un contrôle fin sur les fonctionnalités spécifiques au format, telles que la modification de `RotationOrder` dans l'exportateur FBX. Bien qu'il n'y ait pas de API public exposant directement cette fonctionnalité, Aspose.3D for .NET fournit des moyens de réaliser de telles personnalisations grâce à son architecture flexible.
{{% /alert %}}



Voici comment vous pouvez gérer cela dans Aspose.3D:

{{% highlight "csharp" %}}

var rvm = Scene.FromFile(@"F1234.rvm");
rvm.RootNode.Accept((Node node) =>
{
    node.SetProperty("RotationOrder", 1); //set a custom property, exporter will match this to FBX's property.
    return true; //continue to traverse on other nodes 
});

rvm.Save(@"test.fbx");

{{% /highlight %}}

Dans cet exemple:

1. Créez une scène à partir d'un fichier RVM.
1. Visitez tous les nœuds de la scène.
1. Définir la propriété personnalisée: la méthode SetProperty est utilisée pour définir la propriété `RotationOrder`, démontrant comment les mécanismes internes peuvent être utilisés pour contrôler les fonctionnalités spécifiques au format qui ne sont pas directement exposées par le public API.
1. Enregistrer la scène: La scène est enregistrée avec le `RotationOrder` personnalisé.

En utilisant de telles techniques, Aspose.3D permet aux développeurs d'affiner et de contrôler les fonctionnalités spécifiques des formats 3D, en s'assurant que les exigences détaillées et précises sont satisfaites dans diverses applications 3D.