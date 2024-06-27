---
title: Passen Sie Rotation Order in FBX-Datei an
type: docs
weight: 10
url: /de/net/customize-rotation-order-in-fbx-file
description: Mit Aspose.3D for .NET können Entwickler die nativen FBX Eigenschaften wie Rotation Order anpassen.
---
{{% alert color="primary" %}}

Wenn Sie [Aspose.3D for .NET](https://products.aspose.com/3d/net/) verwenden, benötigen Entwickler manchmal eine feine Kontrolle über formats pezi fische Funktionen, z. B. das Ändern der `RotationOrder` im FBX-Exporteur. Während es möglicher weise keine öffentlichen API gibt, die diese Funktional ität direkt anzeigen, bietet Aspose.3D for .NET Möglichkeiten, solche Anpassungen durch seine flexible Architektur zu erreichen.
{{% /alert %}}



So können Sie dies in Aspose.3D handhaben:

{{% highlight "csharp" %}}

var rvm = Scene.FromFile(@"F1234.rvm");
rvm.RootNode.Accept((Node node) =>
{
    node.SetProperty("RotationOrder", 1); //set a custom property, exporter will match this to FBX's property.
    return true; //continue to traverse on other nodes 
});

rvm.Save(@"test.fbx");

{{% /highlight %}}

In diesem Beispiel:

1. Erstellen Sie eine Szene aus einer RVM-Datei.
1. Besuchen Sie alle Knoten in der Szene.
1.   Set custom property: The SetProperty method is used to set the `RotationOrder` property, demonstrating how internal mechanisms can be leveraged to control format-specific features not directly exposed by the public API.
1. Speichern Sie die Szene: Die Szene wird mit den angepassten `RotationOrder` gespeichert.

Durch die Verwendung solcher Techniken können Entwickler mit Aspose.3D spezifische Funktionen von 3D-Formaten optimieren und steuern, um sicher zustellen, dass detaillierte und präzise Anforderungen in verschiedenen 3D-Anwendungen erfüllt werden.