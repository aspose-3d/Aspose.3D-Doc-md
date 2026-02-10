---
title: Lancer et recevoir des ombres sur les géométries 3D
type: docs
weight: 10
url: /fr/python-net/cast-and-receive-shadows-on-3d-geometries/
description: Généralement, certains formats de fichiers 3D peuvent stocker des paramètres liés à l'ombre dans la géométrie comme FBX. En utilisant Aspose.3D for Python via .NET, les développeurs peuvent rendre une image en cartographiant les ombres du point de vue d'une source de lumière. La qualité d'image dépend de la source lumineuse, de l'angle d'élévation et de la distance entre la caméra et les objets géométriques.
---
{{% alert color="primary" %}}

Généralement, certains formats de fichiers 3D peuvent stocker des paramètres liés à l'ombre dans la géométrie comme FBX. En utilisant [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), les développeurs peuvent rendre une image en cartographiant les ombres du point de vue d'une source de lumière. La qualité d'image dépend de la source lumineuse, de l'angle d'élévation et de la distance entre la caméra et les objets géométriques.

{{% /alert %}}
##  **Cast et recevoir de l'ombre**
Par défaut, tous les objets de la scène projettent des ombres à partir d'une source lumineuse. Les développeurs peuvent également recevoir des ombres par objet dans la surface de l'objet. Cet exemple de code révèle comment définir la position de la lumière et des objets de l'appareil photo. Il crée également un plan et place trois objets avec des couleurs et des paramètres d'ombre différents.

Toutes les géométries ont `cast_shadows = True` et `receive_shadows = True`, les ombres de la boîte rouge et du tore coulées sur le plan, la boîte rouge ne recevra pas d'ombres et la boîte bleue ne jettera pas d'ombres.
###  **Échantillon de programmation**
Cet exemple de code jette et reçoit des ombres sur les géométries 3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Rendering-CastAndReceiveShadow-CastAndReceiveShadow.py" >}}


**Render Résultat**

! [Tout le monde: image_alt_text](cast-and-receive-shadows-on-3d-geometries_1.png)
