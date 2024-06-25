---
title: Agregar la propiedad Animation y configurar la cámara de destino en el documento 3D
type: docs
weight: 10
url: /es/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java admite la representación de escenas animadas. En este artículo se explican los requisitos previos para mover un objeto.
---
##  **Agregar la propiedad Animation en el documento 3D**
Aspose.3D for Java admite la representación de escenas animadas. En este artículo se explican los requisitos previos para mover un objeto.
###  **Mover la posición del cubo**
{{% alert color="primary" %}}

El objeto de clase `Mesh` se está utilizando en el código. Podemos [Crear un objeto de clase Mesh como se narra allí](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) y también debe animar la propiedad de traducción local del nodo: [Adición de la transformación al nodo](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

En Aspose.3D for Java API, la instancia de animación es en realidad una animación de fotogramas clave que se anima en las propiedades. Para animar propiedades, necesita una instancia `CurveMapping` que asigne componentes de una propiedad a diferentes curvas, por ejemplo, una propiedad `Vector3` puede tener 3 componentes `X`/`Y`/`Z`, que configurará tres canales en `CurveMapping`, cada canal puede tener un conjunto de `Curve`.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
##  **Configurar la cámara de destino en el archivo 3D**
Aspose.3D for Java ofrece configurar la cámara objetivo en el archivo 3D. En algunos formatos de archivo, light/camera admite target, lo que permite que la luz/cámara siempre se enfrente a un nodo específico, esto es útil en animación.

{{% alert color="primary" %}}

Las clases `Scene`, `Camera`, `Node` y `Transform` están siendo utilizadas en el código. Para guardar un método `Scene`, `Scene.save`, acepta un nombre de archivo con la ruta completa y el parámetro `FileFormat`.

{{% /alert %}}

En el siguiente ejemplo, el objetivo y la cámara se configuran en el archivo 3D:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
