---
title: Wenden Sie visuelle Effekte an, um 3D-Ansichten zu speichern
type: docs
weight: 10
url: /de/python-net/apply-visual-effects-on-saving-3d-views/
description: Mit Aspose.3D for Python via .NET API können Entwickler visuelle Effekte auf 3D Ansichten anwenden, bevor sie im Bild speichern. Diese visuellen Effekte werden auch als Nach verarbeitung effekte oder Filter bezeichnet, die in Echtzeit auf alles angewendet werden, was in der 3D-Ansicht angezeigt wird.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for Python via .NET API](https://products.aspose.com/3d/python-net/) können Entwickler visuelle Effekte auf 3D Ansichten anwenden, bevor sie im Bild speichern. Diese visuellen Effekte werden auch als Nach verarbeitung effekte oder Filter bezeichnet, die in Echtzeit auf alles angewendet werden, was in der 3D-Ansicht angezeigt wird.

{{% /alert %}}
##  **Visuelle Effekte auf 3D View anwenden**
Die [`get_post_processing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing)-Methode der [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer)-Klasse ermöglicht es, jeden unterstützten visuellen Effekt zu erstellen. Die `Renderer`-Klasse bietet ein [`post_processings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings)-Mitglied, um verschiedene Filter anzuwenden. Die Add-Methode der `PostProcessings`-Klasse ermöglicht es, einen Filter vor dem Rendern einzubauen.
###  **Programmier probe**
Dieses Code beispiel wendet einen visuellen Effekt auf eine 3D-Ansicht an.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.py" >}}
