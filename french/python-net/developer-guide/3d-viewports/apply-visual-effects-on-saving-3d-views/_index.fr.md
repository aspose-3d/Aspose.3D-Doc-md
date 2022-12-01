---
title: Appliquer des effets visuels pour économiser 3D vues
type: docs
weight: 10
url: /fr/python-net/apply-visual-effects-on-saving-3d-views/
description: En utilisant Aspose.3D pour Python via .NET API, les développeurs peuvent appliquer des effets visuels sur 3D Vues avant d'enregistrer dans l'image. Ces effets visuels sont également connus sous le nom d'effets de post-traitement ou de filtres qui sont appliqués en temps réel à tout ce qui est affiché dans la vue 3D.
---
{{% alert color="primary" %}}

Utilisation[Aspose.3D pour Python via .NET API](https://products.aspose.com/3d/python-net/), Les développeurs peuvent appliquer des effets visuels sur les vues 3D avant de les enregistrer dans l'image. Ces effets visuels sont également connus sous le nom d'effets de post-traitement ou de filtres qui sont appliqués en temps réel à tout ce qui est affiché dans la vue 3D.

{{% /alert %}}
## **Appliquer les effets visuels sur 3D View**
La méthode [`get_post_processing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing) de la classe [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer) permet de créer n'importe quel effet visuel pris en charge. La classe `Renderer` offre un membre [`post_processings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings) pour appliquer divers filtres, la méthode Add de la classe `PostProcessings` permet d'incorporer un filtre avant le rendu.
### **Échantillon de programmation**
Cet exemple de code applique un effet visuel sur une vue 3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.py" >}}
