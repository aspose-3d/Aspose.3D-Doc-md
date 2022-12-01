﻿---
title: Rendu basé sur le matériel de la géométrie 3D
type: docs
weight: 30
url: /fr/python-net/hardware-based-rendering-of-3d-geometry/
description: En utilisant Aspose.3D pour Python via .NET API, les développeurs peuvent programmer le GPU (unité de traitement graphique) et configurer le matériel graphique pour rendre la géométrie 3D au lieu du pipeline de fonctions fixes.
---
{{% alert color="primary" %}}

Utilisation[Aspose.3D pour Python via .NET](https://products.aspose.com/3d/python-net/)API, les développeurs peuvent programmer le GPU (unité de traitement graphique) et configurer le matériel graphique pour rendre la géométrie 3D au lieu du pipeline de fonctions fixes. Dans cet article, nous nous concentrons sur le rendu basé sur le matériel en utilisant[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Aspx),[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). Aspx) et[Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
## **Créer du matériel et Rendre une géométrie 3D**
Pour rendre une géométrie 3D, un shader, des tampons et un état de rendu sont requis. Aucun d'entre eux ne peut travailler les uns sans les autres.

- **Tampons**-Les listes de triangles sont des triangles individuels spécifiés dans un tableau parfois appelé tampon. Dans une liste de triangle, chaque triangle est spécifié individuellement. Les points d'un triangle peuvent être partagés en utilisant des indices pour réduire la quantité de données qui doivent être transmises au matériel graphique.
- **Omandeurs**-Il définit comment transformer les triangles de l'espace du monde dans l'espace de l'écran et calculer la couleur finale du pixel dans le côté GPU
- **Rendre les États**-Il fournit des paramètres pour le GPU pour rastériser les triangles en pixels.

{{% alert color="primary" %}}

Nous avons préparé un projet de démonstration. Veuillez vous référer à[Cette URL de téléchargement](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

Le langage d'ombrage OpenGL (GLSL) est le langage d'ombrage standard de haut niveau pour les graphiques OpenGL API. Il existe trois types de shader couramment utilisés: Vertex Shaders, Fragment Shaders et Geometry Shaders.

La classe [`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) indique au moteur de rendu, le code source est pour le langage d'ombrage OpenGL, il peut être compilé en classe [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram). La classe [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) définit les variables utilisées dans le shader. La classe `VariableSemantic` est utilisée pour identifier la sémantique de la variable shader, le moteur de rendu Aspose.3D préparera automatiquement les valeurs de la variable shader en fonction de la sémantique.
### **Échantillon de programmation pour Shader**
Cet exemple de code initialise le renderer et Shader pour la grille. Vous pouvez télécharger le projet de travail complet de cet exemple à partir de[Ici](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Controls-RenderView-RenderView.py" >}}
### **Échantillon de programmation pour l'état du tampon et du déposant**
Cet exemple de code initialise l'état de mémoire tampon et de rendu pour la grille.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Grid-ManualEntity.py" >}}
