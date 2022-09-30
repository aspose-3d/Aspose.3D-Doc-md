---
title: Reparto y recepción de sombras en 3D Geometrías
type: docs
weight: 10
url: /es/net/cast-and-receive-shadows-on-3d-geometries/
description: Generalmente, algunos formatos de archivo 3D pueden almacenar configuraciones relacionadas con la sombra en geometría como FBX. Usando Aspose.3D for .NET, los desarrolladores pueden representar una imagen mapeando sombras desde el punto de vista de una fuente de luz. La calidad de imagen depende de la fuente de luz, el ángulo de elevación y la distancia entre la cámara y los objetos geométricos.
---
{{% alert color="primary" %}}

Generalmente, algunos formatos de archivo 3D pueden almacenar configuraciones relacionadas con la sombra en geometría como FBX. Uso[Aspose.3D for .NET](https://products.aspose.com/3d/net/), Los desarrolladores pueden representar una imagen mapeando sombras desde el punto de vista de una fuente de luz. La calidad de imagen depende de la fuente de luz, el ángulo de elevación y la distancia entre la cámara y los objetos geométricos.

{{% /alert %}}
## **Reparto y recepción de sombra**
Por defecto, todos los objetos de la escena proyectan sombras desde una fuente de luz. Los desarrolladores también pueden recibir sombras por objeto en la superficie del objeto. Este ejemplo de código revela cómo establecer la posición de la luz y los objetos de la cámara. También crea un plano y coloca tres objetos con diferentes colores y configuraciones de sombra.

Todas las geometrías tienen `CastShadows = true` y `ReceiveShadows=true`, las sombras de la caja roja y el toro en el plano, la caja roja no recibirá sombras y la caja azul no proyectará sombras.
### **Muestra de programación**
Este ejemplo de código emite y recibe sombras en 3D geometrías.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Rendering-CastAndReceiveShadow-CastAndReceiveShadow.cs" >}}


**Resultado de renderizado**

![Todo: imagen_Alt_Texto](cast-and-receive-shadows-on-3d-geometries_1.png)
