---
title: Agregar propiedad de animación y configurar cámara de destino en el documento 3D
type: docs
weight: 10
url: /es/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java admite la representación de escenas animadas. Este artículo explica los requisitos previos para mover un objeto.
---
## **Agregar propiedad Animation en el documento 3D**
Aspose.3D for Java admite la representación de escenas animadas. Este artículo explica los requisitos previos para mover un objeto.
### **Mover la posición del cubo**
{{% alert color="primary" %}}

El objeto de clase `Mesh` se está utilizando en el código. Podemos[Crear un objeto de clase Mesh como se narra allí](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/)Y también debe animar la propiedad de traducción local del nodo:[Adición de la transformación al nodo](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

En Aspose.3D for Java API, la instancia de animación es en realidad una animación de fotograma clave que anima las propiedades. Para animar las propiedades, necesita una instancia `CurveMapping` que asigne componentes de una propiedad a diferentes curvas, por ejemplo, una propiedad `Vector3` puede tener 3 componentes `X`/`Y`/`Z`, que configurará tres canales en `CurveMapping`, cada canal puede tener un conjunto de `Curve`.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
## **Configure la cámara de destino en el archivo 3D**
Aspose.3D for Java ofrece configurar la cámara de destino en el archivo 3D. En algunos formatos de archivo, la luz/cámara es compatible con el objetivo, lo que permite que la luz/cámara siempre frente a un nodo específico, esto es útil en animación.

{{% alert color="primary" %}}

Las clases `Scene`, `Camera`, `Node` y `Transform` se están utilizando en el código. Para guardar un método `Scene`, `Scene.save` que se está utilizando, acepta un nombre de archivo con una ruta de acceso completa y un parámetro `FileFormat`.

{{% /alert %}}

En el siguiente ejemplo, el objetivo y la cámara se configuran en el archivo 3D:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
