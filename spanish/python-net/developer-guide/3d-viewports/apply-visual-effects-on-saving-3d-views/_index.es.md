---
title: Aplicar efectos visuales al guardar las vistas 3D
type: docs
weight: 10
url: /es/python-net/apply-visual-effects-on-saving-3d-views/
description: Usando Aspose.3D for Python via .NET API, los desarrolladores pueden aplicar efectos visuales en 3D Vistas antes de guardar en la imagen. Estos efectos visuales también se conocen como efectos de posprocesamiento o filtros que se aplican en tiempo real a todo lo que se muestra en la vista 3D.
---
{{% alert color="primary" %}}

Con [Aspose.3D for Python via .NET API](https://products.aspose.com/3d/python-net/), los desarrolladores pueden aplicar efectos visuales en las vistas de 3D antes de guardar la imagen. Estos efectos visuales también se conocen como efectos de posprocesamiento o filtros que se aplican en tiempo real a todo lo que se muestra en la vista 3D.

{{% /alert %}}
##  **Aplicar efectos visuales en la vista 3D**
El método [`get_post_processing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing) de la clase [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer) permite crear cualquier efecto visual admitido. La clase `Renderer` ofrece un miembro [`post_processings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings) para aplicar varios filtros, el método Add de la clase `PostProcessings` permite incorporar un filtro antes de renderizar.
###  **Muestra de programación**
Este ejemplo de código aplica el efecto visual en una vista 3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.py" >}}
