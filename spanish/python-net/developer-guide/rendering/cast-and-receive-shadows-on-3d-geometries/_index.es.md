---
title: Reparto y recepción de sombras en geometrías 3D
type: docs
weight: 10
url: /es/python-net/cast-and-receive-shadows-on-3d-geometries/
description: En general, algunos formatos de archivo 3D pueden almacenar configuraciones relacionadas con la sombra en geometría como FBX. Usando Aspose.3D for Python via .NET, los desarrolladores pueden renderizar una imagen mapeando sombras desde el punto de vista de una fuente de luz. La calidad de la imagen depende de la fuente de luz, el ángulo de elevación y la distancia entre la cámara y los objetos geométricos.
---
{{% alert color="primary" %}}

En general, algunos formatos de archivo 3D pueden almacenar configuraciones relacionadas con la sombra en geometría como FBX. Usando [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), los desarrolladores pueden renderizar una imagen mapeando sombras desde el punto de vista de una fuente de luz. La calidad de la imagen depende de la fuente de luz, el ángulo de elevación y la distancia entre la cámara y los objetos geométricos.

{{% /alert %}}
##  **Reparto y recepción de sombra**
Por defecto, todos los objetos de la escena proyectan sombras desde una fuente de luz. Los desarrolladores también pueden recibir sombras por objeto en la superficie del objeto. Este ejemplo de código revela cómo establecer la posición de la luz y los objetos de la cámara. También crea un plano y coloca tres objetos con diferentes colores y configuraciones de sombra.

Todas las geometrías tienen `cast_shadows = True` y `receive_shadows = True`, las sombras de la caja roja y el toro se proyectan en el plano, la caja roja no recibirá sombras y la caja azul no proyectará sombras.
###  **Muestra de programación**
Este ejemplo de código proyecta y recibe sombras en geometrías 3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Rendering-CastAndReceiveShadow-CastAndReceiveShadow.py" >}}


**Resultado de renderizado**

¡! [Todo: image_alt_text](cast-and-receive-shadows-on-3d-geometries_1.png)
