---
title: Agregar la propiedad Animation y configurar la cámara de destino en el documento 3D
type: docs
weight: 10
url: /es/python-net/add-animation-property-and-setup-target-camera-in-3d-document/
description: En Aspose.3D, la animación de objetos es en realidad una animación de fotogramas clave que se anima en las propiedades. Para animar las propiedades, necesita una instancia de CurveMapping que asigne los componentes de una propiedad a diferentes curvas, por ejemplo, una propiedad Vector3 puede tener 3 componentes X/Y/Z, que configurará tres canales en CurveMapping, cada canal puede tener un conjunto de curvas.
---
##  **Agregar la propiedad Animation en el documento 3D**
Aspose.3D for Python via .NET admite la representación de escenas animadas. En este artículo se explican los requisitos previos para mover un objeto.
###  **Mover la posición del cubo**
{{% alert color="primary" %}}

El objeto de clase [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) se está utilizando en el código. Podemos [Crear un objeto de clase Mesh como se narra allí](/3d/es/net/create-and-read-an-existing-3d-scene/) y también debe animar la propiedad de traducción local del nodo: [Adición de la transformación al nodo](/3d/es/net/adding-transformation-to-the-node/).

{{% /alert %}}

En Aspose.3D, la animación de objetos es en realidad una animación de fotogramas clave que se anima en las propiedades. Para animar propiedades, necesita una instancia `CurveMapping` que asigne componentes de una propiedad a diferentes curvas, por ejemplo, una propiedad `Vector3` puede tener 3 componentes `X`/`Y`/`Z`, que configurará tres canales en `CurveMapping`, cada canal puede tener un conjunto de `Curve`.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Animation-PropertyToDocument-AddAnimationPropertyToDocument.py" >}}
##  **Configurar la cámara de destino en el archivo 3D**
Aspose.3D for Python via .NET ofrece configurar la cámara de destino en el archivo 3D. En algunos formatos de archivo, light/camera admite target, lo que permite que la luz/cámara siempre se enfrente a un nodo específico, esto es útil en animación.

{{% alert color="primary" %}}

Las clases [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) y [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) están siendo utilizadas en el código. Para guardar un método Scene, se está utilizando el método [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save), acepta un nombre de archivo con la ruta completa y el parámetro [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat).

{{% /alert %}}

En el siguiente ejemplo, el objetivo y la cámara se configuran en el archivo 3D:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Animation-SetupTargetAndCamera-SetupTargetAndCamera.py" >}}
