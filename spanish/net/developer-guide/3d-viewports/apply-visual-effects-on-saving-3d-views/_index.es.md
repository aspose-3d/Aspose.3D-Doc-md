---
title: Aplicar efectos visuales al guardar vistas 3D
type: docs
weight: 10
url: /es/net/apply-visual-effects-on-saving-3d-views/
description: Usando Aspose.3D for .NET API, los desarrolladores pueden aplicar efectos visuales en las vistas 3D antes de guardar en la imagen. Estos efectos visuales también se conocen como efectos o filtros de posprocesamiento que se aplican en tiempo real a todo lo que se muestra en la vista 3D.
---
{{% alert color="primary" %}}

Uso[Aspose.3D for .NET API](https://products.aspose.com/3d/net/), Los desarrolladores pueden aplicar efectos visuales en las vistas 3D antes de guardar en la imagen. Estos efectos visuales también se conocen como efectos o filtros de posprocesamiento que se aplican en tiempo real a todo lo que se muestra en la vista 3D.

{{% /alert %}}
## **Aplicar efectos visuales en la vista 3D**
El método [`GetPostProcessing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing) de la clase [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer) permite crear cualquier efecto visual compatible. La clase Renderer ofrece un miembro [`PostProcessings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings) para aplicar varios filtros, el método Add de la clase PostProcessings permite incorporar un filtro antes de renderizar.
### **Muestra de programación**
Este ejemplo de código aplica un efecto visual en una vista 3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.cs" >}}
