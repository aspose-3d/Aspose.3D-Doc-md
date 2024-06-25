---
title: Wenden Sie visuelle Effekte an, um 3D-Ansichten zu speichern
type: docs
weight: 10
url: /de/net/apply-visual-effects-on-saving-3d-views/
description: Mit Aspose.3D for .NET API können Entwickler visuelle Effekte auf 3D Ansichten anwenden, bevor sie im Bild speichern. Diese visuellen Effekte werden auch als Nach bearbeitungs effekte oder Filter bezeichnet, die in Echtzeit auf alles angewendet werden, was in der 3D-Ansicht angezeigt wird.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for .NET API](https://products.aspose.com/3d/net/) können Entwickler visuelle Effekte auf 3D Ansichten anwenden, bevor sie im Bild speichern. Diese visuellen Effekte werden auch als Nach verarbeitung effekte oder Filter bezeichnet, die in Echtzeit auf alles angewendet werden, was in der 3D-Ansicht angezeigt wird.

{{% /alert %}}
##  **Visuelle Effekte auf 3D View anwenden**
Die [`GetPostProcessing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing)-Methode der [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer)-Klasse ermöglicht es, jeden unterstützten visuellen Effekt zu erstellen. Die Renderer-Klasse bietet ein [`PostProcessings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings)-Mitglied zum Anwenden verschiedener Filter. Die Add-Methode der PostProcessings-Klasse ermöglicht es, vor dem Rendern einen Filter einzubauen.
###  **Programmier probe**
Dieses Code beispiel wendet einen visuellen Effekt auf eine 3D-Ansicht an.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.cs" >}}
