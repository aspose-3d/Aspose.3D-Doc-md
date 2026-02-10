---
title: Ajouter une hiérarchie de nœud et partager des données géométriques de maillage entre plusieurs nœuds de la scène 3D
type: docs
weight: 20
url: /fr/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java a le support de la construction d'une hiérarchie de nœuds. Le nœud est un bloc de construction de base de la scène 3D et une hiérarchie de nœuds définit la structure logique de la scène 3D et fournit un contenu visible en attachant des géométries, des lumières et des caméras aux nœuds.
---
##  **Ajouter une hiérarchie de nœud dans le document de scène 3D**
Aspose.3D for Java a le support de la construction d'une hiérarchie de nœuds. Le `Node` est le bloc de construction de base de la scène 3D et une hiérarchie de nœuds définit la structure logique de la scène 3D et fournit un contenu visible en attachant des géométries, des lumières et des caméras aux nœuds.
###  **Exemple de graphique de scène**

Dans Aspose.3D, chaque instance `Node` peut avoir plusieurs nœuds enfants, dans cet exemple, nous avons créé un nœud avec deux nœuds cubes, si nous faisons pivoter le nœud racine, tous les nœuds enfants sont également affectés:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Get a child node object
Node top = scene.getRootNode().createChildNode();
// Each cube node has their own translation
Node cube1 = top.createChildNode("cube1");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the mesh
cube1.setEntity(mesh);
// Set first cube translation
cube1.getTransform().setTranslation(new Vector3(-10, 0, 0));
Node cube2 = top.createChildNode("cube2");
// Point node to the mesh
cube2.setEntity(mesh);
// Set second cube translation
cube2.getTransform().setTranslation(new Vector3(10, 0, 0));
// The rotated top node will affect all child nodes
top.getTransform().setRotation(Quaternion.fromEulerAngle(Math.PI, 4, 0));
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("NodeHierarchy.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
##  **Partager les données de géométrie du maillage entre plusieurs nœuds**
Afin de diminuer les nécessités de mémoire, une seule instance de `Mesh` Class peut être liée à diverses instances de `Node` Class. Envisagent que vous avez besoin d'un système où tous les 3D cubes semblaient être indiscernables, mais vous en aviez besoin d'un grand nombre. Vous pouvez épargner de la mémoire en faisant un objet Mesh lorsque le système démarre. À ce stade, chaque fois que vous avez besoin d'une autre forme, vous faites un autre objet Node, puis pointez ce nœud vers celui `Mesh`. C'est ce que l'on appelle l'instanciation. Aspose.3D for Java Les API permettent de faire de l'instanciation.
###  **Exemple d'instantanement**
Dans les jeux RTS (stratégie en temps réel) comme, nous pouvons toujours voir plusieurs PNJ (personnage non joueur) avec le même modèle 3D, peut-être dans des couleurs différentes, le moteur de rendu partage généralement les mêmes données de géométrie de maillage à travers différents PNJ, cette technique s'appelle Instancing.

{{% alert color="primary" %}} 

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons [Créer un objet de classe Mesh tel que raconté là-bas](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Démonstration de l'exemple de code:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Define color vectors
Vector3[] colors = new Vector3[] {
    new Vector3(1, 0, 0),
    new Vector3(0, 1, 0),
    new Vector3(0, 0, 1)
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
int idx = 0;
for(Vector3 color : colors)
{
    // Initialize cube node object
    Node cube = new Node("cube");
    cube.setEntity(mesh);
    LambertMaterial mat = new LambertMaterial();
    // Set color
    mat.setDiffuseColor(color);
    // Set material
    cube.setMaterial(mat);
    // Set translation
    cube.getTransform().setTranslation(new Vector3(idx++ * 20, 0, 0));
    // Add cube node
    scene.getRootNode().addChildNode(cube);
}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("MeshGeometryData.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}


Dans cet exemple, nous avons créé 3 nœuds cubes partagent le même maillage, chacun d'eux a un matériau différent avec des couleurs différentes.
