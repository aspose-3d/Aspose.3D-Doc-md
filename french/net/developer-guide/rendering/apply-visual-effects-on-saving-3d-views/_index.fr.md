---
title: Appliquer des effets visuels sur les vues de Saving 3D
type: docs
weight: 10
url: /fr/net/apply-visual-effects-on-saving-3d-views/
description: En utilisant Aspose.3D for .NET API, les développeurs peuvent appliquer des effets visuels sur les vues 3D avant de les enregistrer dans l'image. Ces effets visuels sont également connus sous le nom d'effets de post-traitement ou de filtres qui sont appliqués en temps réel à tout ce qui est affiché dans la vue 3D.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET API](https://products.aspose.com/3d/net/), les développeurs peuvent appliquer des effets visuels sur les vues 3D avant d'enregistrer dans l'image. Ces effets visuels sont également connus comme les effets de post-traitement ou les filtres qui sont appliqués en temps réel à tout ce qui s'affiche dans la vue 3D.

{{% /alert %}}
##  **Appliquer des effets visuels sur 3D Voir**
La méthode [`GetPostProcessing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing) de la classe [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer) permet de créer n'importe quel effet visuel pris en charge. La classe Renderer offre un membre [`PostProcessings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings) pour appliquer différents filtres, la méthode Add de la classe PostProcessings permet d'incorporer un filtre avant le rendu.
###  **Échantillon de programmation**
Cet exemple de code applique un effet visuel sur une vue 3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.cs" >}}
