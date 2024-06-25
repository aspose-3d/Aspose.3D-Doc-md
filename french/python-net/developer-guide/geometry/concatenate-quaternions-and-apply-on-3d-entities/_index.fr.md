---
title: Concaténer les quaternions et appliquer sur les entités 3D
type: docs
weight: 50
url: /fr/python-net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for Python via .NET permet aux développeurs de combiner deux transformation de rotation en une seule représentée dans un quaternion.
---
{{% alert color="primary" %}} 

[Aspose.3D for Python via .NET](https://www.aspose.com/products/3d) permet aux développeurs de combiner deux transformation de rotation en une seule représentée dans un quaternion.

{{% /alert %}} 
##  **Quaternions concaténer**
Les quaternions sont utilisés pour représenter une orientation dans l'espace 3D. La méthode `concat` exposée par la classe [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion) peut être utilisée pour combiner deux quaternions. Dans cet exemple de code, nous combinons deux quaternions et obtenons un troisième quaternion résultant, puis nous appliquons ces trois quaternions à trois cylindres.
###  **Échantillon de programmation**
Cet exemple de code combine deux quaternions et les applique à différents cylindres.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-ConcatenateQuaternions-ConcatenateQuaternions.py" >}}


**Résultat dans 3ds MAX**

! [Tout le monde: image_alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
