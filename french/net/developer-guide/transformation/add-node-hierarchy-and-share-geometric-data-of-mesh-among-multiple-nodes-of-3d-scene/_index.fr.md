---
title: Ajouter une hiérarchie de nœud et partager des données géométriques de maillage entre plusieurs nœuds de la scène 3D
type: docs
weight: 40
url: /fr/net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for .NET propose de construire une hiérarchie de nœuds. Le nœud est le bloc de construction de base d'une scène. Une hiérarchie de nœuds définit la structure logique d'une scène et fournit un contenu visible en attachant des géométries, des lumières et des caméras aux nœuds.
---
##  **Ajouter une hiérarchie de nœud dans le document de scène 3D**
Aspose.3D for .NET propose de construire une hiérarchie de nœuds. Le nœud est le bloc de construction de base d'une scène. Une hiérarchie de nœuds définit la structure logique d'une scène et fournit un contenu visible en attachant des géométries, des lumières et des caméras aux nœuds.
###  **Exemple de graphique de scène**
Un exemple de hiérarchie de scène ressemble à:

! [Tout le monde: image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

Dans Aspose.3D, chaque instance `Node` peut avoir plusieurs nœuds enfants, dans cet exemple, nous avons créé un nœud avec deux nœuds cubes, si nous faisons pivoter le nœud racine, tous les nœuds enfants sont également affectés:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Get a child node object
Node top = scene.RootNode.CreateChildNode();
// Each cube node has their own translation
Node cube1 = top.CreateChildNode("cube1");
// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();            
// Point node to the mesh
cube1.Entity = mesh;
// Set first cube translation
cube1.Transform.Translation = new Vector3(-10, 0, 0);
Node cube2 = top.CreateChildNode("cube2");
// Point node to the mesh
cube2.Entity = mesh;
// Set second cube translation
cube2.Transform.Translation = new Vector3(10, 0, 0);

// The rotated top node will affect all child nodes
top.Transform.Rotation = Quaternion.FromEulerAngle(Math.PI, 4, 0);
          
// Save 3D scene in the supported file formats
scene.Save("NodeHierarchy.fbx");

{{< /highlight >}}
##  **Partager les données de géométrie du maillage entre plusieurs nœuds**
Pour diminuer les nécessités de mémoire, une seule instance de [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) Class peut être liée à diverses instances de [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) Class. Envisagent que vous avez besoin d'un système où tous les 3D cubes semblaient être indiscernables, mais vous en aviez besoin d'un grand nombre. Vous pouvez épargner de la mémoire en faisant un objet Mesh lorsque le système démarre. À ce stade, chaque fois que vous avez besoin d'une autre forme, vous faites un autre objet Node, puis pointez ce nœud vers le maillage. C'est ce que l'on appelle l'instanciation. Les API Aspose.3D for .NET permettent de faire l'instanciation.
###  **Exemple d'instantanement**
Dans les jeux RTS (stratégie en temps réel) comme, nous pouvons toujours voir plusieurs PNJ (personnage non joueur) avec le même modèle 3D, peut-être dans des couleurs différentes, le moteur de rendu partage généralement les mêmes données de géométrie de maillage à travers différents PNJ, cette technique s'appelle Instancing.

{{% alert color="primary" %}}

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons [Créer un objet de classe Mesh tel que raconté là-bas](/3d/fr/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Démonstration de l'exemple de code:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();

// Define color vectors
Vector3[] colors = new Vector3[] {
new Vector3(1, 0, 0),
new Vector3(0, 1, 0),
new Vector3(0, 0, 1)
};

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
           
int idx = 0;
foreach (Vector3 color in colors)
{
    // Initialize cube node object
    Node cube = new Node("cube");
    cube.Entity = mesh;
    LambertMaterial mat = new LambertMaterial();
    // Set color
    mat.DiffuseColor = color;
    // Set material
    cube.Material = mat;
    // Set translation
    cube.Transform.Translation = new Vector3(idx++ * 20, 0, 0);
    // Add cube node
    scene.RootNode.ChildNodes.Add(cube);
}
        
// Save 3D scene in the supported file formats
scene.Save("MeshGeometryData.fbx");

{{< /highlight >}}

Dans cet exemple, nous avons créé 3 nœuds cubes partagent le même maillage, chacun d'eux a un matériau différent avec des couleurs différentes.
