---
title: Ajouter une propriété d'animation et configurer la caméra cible dans le document 3D
type: docs
weight: 10
url: /fr/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java prend en charge le rendu des scènes animées. Cet article explique les conditions préalables pour déplacer un objet.
---
##  **Ajouter la propriété Animation dans le document 3D**
Aspose.3D for Java prend en charge le rendu des scènes animées. Cet article explique les conditions préalables pour déplacer un objet.
###  **Déplacer la position du cube**
{{% alert color="primary" %}}

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons [Créer un objet de classe Mesh tel que raconté là-bas](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) et il doit aussi animer la propriété de traduction locale du nœud: [Ajout de la transformation au nœud](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

Dans Aspose.3D for Java API, l'instance d'animation est en fait une animation d'image clé qui s'anime sur les propriétés. Pour animer les propriétés, vous avez besoin d'une instance `CurveMapping` qui mappe les composants d'une propriété à différentes courbes, par exemple, une propriété `Vector3` peut avoir 3 composants `X`/`Y`/`Z`, qui mettra en place trois canaux dans `CurveMapping`, chaque canal peut avoir un ensemble de `Curve`.

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
##  **Configurer la caméra cible dans le fichier 3D**
Aspose.3D for Java propose de configurer la caméra cible dans le fichier 3D. Dans certains formats de fichiers, la lumière/caméra prend en charge la cible, ce qui permet à la lumière/caméra toujours face à un nœud spécifié, ce qui est utile dans l'animation.

{{% alert color="primary" %}}

Les classes `Scene`, `Camera`, `Node` et `Transform` sont utilisées dans le code. Pour enregistrer une méthode `Scene`, `Scene.save`, elle accepte un nom de fichier avec le chemin complet et le paramètre `FileFormat`.

{{% /alert %}}

Dans l'exemple ci-dessous, la cible et la caméra sont configurés dans le fichier 3D:

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
