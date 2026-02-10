---
title: Agregar la propiedad Animation y configurar la cámara de destino en el documento 3D
type: docs
weight: 10
url: /es/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: En Aspose.3D, la animación de objetos es en realidad una animación de fotogramas clave que se anima en las propiedades. Para animar las propiedades, necesita una instancia de CurveMapping que asigne los componentes de una propiedad a diferentes curvas, por ejemplo, una propiedad Vector3 puede tener 3 componentes X/Y/Z, que configurará tres canales en CurveMapping, cada canal puede tener un conjunto de curvas.
---
##  **Agregar la propiedad Animation en el documento 3D**
Aspose.3D for .NET admite la representación de escenas animadas. En este artículo se explican los requisitos previos para mover un objeto.
###  **Mover la posición del cubo**
{{% alert color="primary" %}}

El objeto de clase [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) se está utilizando en el código. Podemos [Crear un objeto de clase Mesh como se narra allí](/3d/es/net/create-and-read-an-existing-3d-scene/) y también debe animar la propiedad de traducción local del nodo: [Adición de la transformación al nodo](/3d/es/net/adding-transformation-to-the-node/).

{{% /alert %}}

En Aspose.3D, la animación de objetos es en realidad una animación de fotogramas clave que se anima en las propiedades. Para animar propiedades, necesita una instancia `CurveMapping` que asigne componentes de una propiedad a diferentes curvas, por ejemplo, una propiedad `Vector3` puede tener 3 componentes `X`/`Y`/`Z`, que configurará tres canales en `CurveMapping`, cada canal puede tener un conjunto de `Curve`.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();             

// Each cube node has their own translation
Node cube1 = scene.RootNode.CreateChildNode("cube1", mesh);

// Find translation property on node's transform object
Property translation = cube1.Transform.FindProperty("Translation");
            
// Create a bind point based on translation property
BindPoint bindPoint = new BindPoint(scene, translation);

// Create the animation curve on X component of the scale 
bindPoint.BindKeyframeSequence("X", new KeyframeSequence()
{
    // Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
    {0, 10.0f, Interpolation.Bezier},
    // Move node's translation to (20, 0, -10) at 3 sec
    {3, 20.0f, Interpolation.Bezier},
    // Move node's translation to (30, 0, 0) at 5 sec
    {5, 30.0f, Interpolation.Linear},
});

// Create the animation curve on Z component of the scale 
bindPoint.BindKeyframeSequence("Z", new KeyframeSequence()
{
    // Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
    {0, 10.0f, Interpolation.Bezier},
    // Move node's translation to (20, 0, -10) at 3 sec
    {3, -10.0f, Interpolation.Bezier},
    // Move node's translation to (30, 0, 0) at 5 sec
    {5, 0.0f, Interpolation.Linear},
});

// Save 3D scene in the supported file formats
scene.Save("PropertyToDocument.fbx");

{{< /highlight >}}
##  **Configurar la cámara de destino en el archivo 3D**
Aspose.3D for .NET ofrece configurar la cámara objetivo en el archivo 3D. En algunos formatos de archivo, light/camera admite target, lo que permite que la luz/cámara siempre se enfrente a un nodo específico, esto es útil en animación.

{{% alert color="primary" %}}

Las clases [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) y [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) están siendo utilizadas en el código. Para guardar un método `Scene`, [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save), acepta un nombre de archivo con ruta completa y parámetro [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat).

{{% /alert %}}

En el siguiente ejemplo, el objetivo y la cámara se configuran en el archivo 3D:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
// Get a child node object
Node cameraNode = scene.RootNode.CreateChildNode("camera", new Camera());
// Set camera node translation
cameraNode.Transform.Translation = new Vector3(100, 20, 0);
cameraNode.GetEntity<Camera>().Target = scene.RootNode.CreateChildNode("target");
scene.Save("camera-test.3ds");

{{< /highlight >}}
