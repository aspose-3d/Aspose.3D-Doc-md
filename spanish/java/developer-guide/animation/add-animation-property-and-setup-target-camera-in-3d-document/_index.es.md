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

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize scene object
Scene scene = new Scene();

// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();

// Each cube node has their own translation
Node cube1 = scene.getRootNode().createChildNode("cube1", mesh);

// Find translation property on node's transform object
Property translation = cube1.getTransform().findProperty("Translation");

// Create a bind point based on translation property
BindPoint bindPoint = new BindPoint(scene, translation);

// Create the animation curve on X component of the scale
KeyframeSequence kfs = new KeyframeSequence();
// Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
kfs.add(0, 10.0f, Interpolation.BEZIER);
// Move node's translation to (20, 0, -10) at 3 sec
kfs.add(3, 20.0f, Interpolation.BEZIER);
// Move node's translation to (30, 0, 0) at 5 sec
kfs.add(5, 30.0f, Interpolation.LINEAR);
            
bindPoint.bindKeyframeSequence("X", kfs);

kfs = new  KeyframeSequence();
// Move node's translation to (10, 0, 10) at 0 sec using bezier interpolation
kfs.add(0, 10.0f, Interpolation.BEZIER);
// Move node's translation to (20, 0, -10) at 3 sec
kfs.add(3, -10.0f, Interpolation.BEZIER);
// Move node's translation to (30, 0, 0) at 5 sec
kfs.add(5, 0.0f, Interpolation.LINEAR);
            
bindPoint.bindKeyframeSequence("Z", kfs);

// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("PropertyToDocument.fbx");

// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);

{{< /highlight >}}
##  **Configurar la cámara de destino en el archivo 3D**
Aspose.3D for Java ofrece configurar la cámara objetivo en el archivo 3D. En algunos formatos de archivo, light/camera admite target, lo que permite que la luz/cámara siempre se enfrente a un nodo específico, esto es útil en animación.

{{% alert color="primary" %}}

Las clases `Scene`, `Camera`, `Node` y `Transform` están siendo utilizadas en el código. Para guardar un método `Scene`, `Scene.save`, acepta un nombre de archivo con la ruta completa y el parámetro `FileFormat`.

{{% /alert %}}

En el siguiente ejemplo, el objetivo y la cámara se configuran en el archivo 3D:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize scene object
Scene scene = new Scene();
// Get a child node object
Node cameraNode = scene.getRootNode().createChildNode("camera", new Camera());
// Set camera node translation
cameraNode.getTransform().setTranslation(new Vector3(100, 20, 0));
((Camera)cameraNode.getEntity()).setTarget(scene.getRootNode().createChildNode("target"));
MyDir = MyDir + "camera-test.3ds";
scene.save(MyDir, FileFormat.DISCREET3DS);
{{< /highlight >}}
