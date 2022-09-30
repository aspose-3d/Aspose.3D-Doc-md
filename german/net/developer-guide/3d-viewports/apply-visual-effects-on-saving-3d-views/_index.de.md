---
title: Visuelle Effekte beim Speichern von 3D-Ansichten anwenden
type: docs
weight: 10
url: /de/net/apply-visual-effects-on-saving-3d-views/
description: Mit Aspose.3D for .NET APIkönnen Entwickler visuelle Effekte auf 3D-Ansichten anwenden, bevor sie im Bild speichern. Diese visuellen Effekte werden auch als Nach bearbeitungs effekte oder Filter bezeichnet, die in Echtzeit auf alles angewendet werden, was in der Ansicht 3D angezeigt wird.
---
{{% alert color="primary" %}}

Verwendung[Aspose.3D for .NET API](https://products.aspose.com/3d/net/)Entwickler können visuelle Effekte auf 3D Views anwenden, bevor sie im Bild gespeichert werden. Diese visuellen Effekte werden auch als Nach bearbeitungs effekte oder Filter bezeichnet, die in Echtzeit auf alles angewendet werden, was in der Ansicht 3D angezeigt wird.

{{% /alert %}}
## **Visuelle Effekte anwenden auf 3D Ansicht**
Die [`GetPostProcessing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing)-Methode der [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer)-Klasse ermöglicht es, jeden unterstützten visuellen Effekt zu erzeugen. Die Renderer-Klasse bietet ein [`PostProcessings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings)-Mitglied zum Anwenden verschiedener Filter. Die Add-Methode der PostProcessings-Klasse ermöglicht das Einbinden eines Filters vor dem Rendern.
### **Programmier probe**
Dieses Code beispiel wendet den visuellen Effekt auf eine Ansicht 3D an.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.cs" >}}
