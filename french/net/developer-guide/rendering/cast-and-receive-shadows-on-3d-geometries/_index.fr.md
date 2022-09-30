---
title: Cast et recevoir des ombres sur les géométries 3D
type: docs
weight: 10
url: /fr/net/cast-and-receive-shadows-on-3d-geometries/
description: En règle générale, certains formats de fichiers 3D peuvent stocker des paramètres liés à l'ombre dans une géométrie comme FBX. En utilisant Aspose.3D for .NET, les développeurs peuvent rendre une image en mappant les ombres du point de vue d'une source de lumière. La qualité de l'image dépend de la source lumineuse, de l'angle d'élévation et de la distance entre l'appareil photo et les objets géométriques.
---
{{% alert color="primary" %}}

En règle générale, certains formats de fichiers 3D peuvent stocker des paramètres liés à l'ombre dans une géométrie comme FBX. Utilisation[Aspose.3D for .NET](https://products.aspose.com/3d/net/), Les développeurs peuvent rendre une image en mappant les ombres du point de vue d'une source lumineuse. La qualité de l'image dépend de la source lumineuse, de l'angle d'élévation et de la distance entre l'appareil photo et les objets géométriques.

{{% /alert %}}
## **Cast et recevoir de l'ombre**
Par défaut, tous les objets de la scène projettent des ombres à partir d'une source lumineuse. Les développeurs peuvent également recevoir des ombres par objet dans la surface de l'objet. Cet exemple de code révèle comment définir la position de la lumière et des objets de l'appareil photo. Il crée également un plan et place trois objets avec des couleurs et des paramètres d'ombre différents.

Toutes les géométries ont `CastShadows = true` et `ReceiveShadows=true`, les ombres de la boîte rouge et du tore coulés à l'avion, la boîte rouge ne recevra pas d'ombres et la boîte bleue ne projettera pas d'ombres.
### **Échantillon de programmation**
Cet exemple de code projette et reçoit des ombres sur les géométries 3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Rendering-CastAndReceiveShadow-CastAndReceiveShadow.cs" >}}


**Render Résultat**

![Todo: image_Alt_Texte](cast-and-receive-shadows-on-3d-geometries_1.png)
