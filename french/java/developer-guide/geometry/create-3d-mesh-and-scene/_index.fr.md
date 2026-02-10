---
title: Créer un maillage et une scène 3D
type: docs
weight: 40
url: /fr/java/create-3d-mesh-and-scene/
description: Un maillage est défini par un ensemble de points de contrôle et les nombreux polygones à n côtés selon les besoins. Cet article explique comment définir un maillage.
---
##  **Créer un maillage de cube 3D**
Un `Mesh` est défini par un ensemble de points de contrôle et les nombreux polygones à n côtés selon les besoins. Cet article explique comment définir un `Mesh`.

Pour créer une surface `Mesh`, nous devons définir les points de contrôle et les polygones comme suit:

- [Définir les points de contrôle](/3d/fr/java/create-3d-mesh-and-scene-html/)
- [Créer des polygones avec PolygonBuilder Classe](/3d/fr/java/create-3d-mesh-and-scene-html/)
- [Créer des polygones](/3d/fr/java/create-3d-mesh-and-scene-html/)

Voici un exemple pour attacher un matériau Phong au nœud cube:
###  **Définir les points de contrôle**
Un maillage est composé d'un ensemble de points de contrôle dans l'espace et de polygones pour décrire la surface maillée, pour créer un maillage, nous devons définir les points de contrôle:

{{% alert color="primary" %}} 

Les points de contrôle de toutes les géométries dans Aspose.3D utilisent la coordonnée homogène, donc c'est `Vector4` au lieu de `Vector3` dans l'exemple de code.

{{% /alert %}} 

**Exemple:**

{{< highlight "java" >}}
// Initialize control points
Vector4List controlPoints = new Vector4List(8);
controlPoints.add(new Vector4( -5.0, 0.0, 5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 0.0, 5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 10.0, 5.0, 1.0));
controlPoints.add(new Vector4( -5.0, 10.0, 5.0, 1.0));
controlPoints.add(new Vector4( -5.0, 0.0, -5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 0.0, -5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 10.0, -5.0, 1.0));
controlPoints.add(new Vector4( -5.0, 10.0, -5.0, 1.0));
{{< /highlight >}}



###  **Créer des polygones**
Les points de contrôle ne sont pas rendables, pour rendre le cube visible, nous devons définir des polygones de chaque côté:

{{< highlight "java" >}}
List<Vector4> controlPoints = defineControlPoints();
// Initialize mesh object
Mesh mesh = new Mesh();
// Add control points to the mesh
mesh.getControlPoints().addAll(controlPoints);
// Create polygons to mesh
// Front face (Z+)
mesh.createPolygon(new int[] { 0, 1, 2, 3 });
// Right side (X+)
mesh.createPolygon(new int[] { 1, 5, 6, 2 });
// Back face (Z-)
mesh.createPolygon(new int[] { 5, 4, 7, 6 });
// Left side (X-)
mesh.createPolygon(new int[] { 4, 0, 3, 7 });
// Bottom face (Y-)
mesh.createPolygon(new int[] { 0, 4, 5, 1 });
// Top face (Y+)
mesh.createPolygon(new int[] { 3, 2, 6, 7 });
{{< /highlight >}}



###  **Créer des polygones avec PolygonBuilder Classe**
Nous pouvons également définir polygone par sommets avec la classe PolygonBuilder:

{{< highlight "java" >}}
List<Vector4> controlPoints = defineControlPoints();
// Initialize mesh object
Mesh mesh = new Mesh();
// Add control points to the mesh
mesh.getControlPoints().addAll(controlPoints);
// Indices of the vertices per each polygon
int[] indices = new int[]
{
    0,1,2,3, // Front face (Z+)
    1,5,6,2, // Right side (X+)
    5,4,7,6, // Back face (Z-)
    4,0,3,7, // Left side (X-)
    0,4,5,1, // Bottom face (Y-)
    3,2,6,7 // Top face (Y+)
};
int vertexId = 0;
PolygonBuilder builder = new PolygonBuilder(mesh);
for (int face = 0; face < 6; face++)
{
    // Start defining a new polygon
    builder.begin();
    for (int v = 0; v < 4; v++)
        // The indice of vertice per each polygon
        builder.addVertex(indices[vertexId++]);
    // Finished one polygon
    builder.end();
}
{{< /highlight >}}

Maintenant, c'est fini, pour rendre le maillage visible, nous devons préparer un nœud pour cela.
##  **Comment trianguler un maillage**
Le maillage triangulé est utile pour l'industrie du jeu car le triangulaire est la seule primitive prise en charge par le matériel GPU (les données non triangulaires sont triangulées au niveau du pilote, ce qui est inefficace en temps réel)

{{% alert color="primary" %}} 

Dans cette version, nous avons seulement triangulé les polygones car il est requis par l'exportation de fichiers 3ds, les normes/uvs et autres éléments de sommet sont perdus au cours de cette procédure, nous pouvons l'implémenter à l'avenir.

{{% /alert %}} 

Dans cet exemple, nous triangulons un Mesh en important un fichier FBX et le sauvegardons au format FBX.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize scene object
Scene scene = new Scene();
scene.open(MyDir + "document.fbx");
scene.getRootNode().accept(new NodeVisitor() {
    @Override
    public boolean call(Node node) {
        Mesh mesh = (Mesh)node.getEntity();
        if (mesh != null)
        {
            // Triangulate the mesh
            Mesh newMesh = PolygonModifier.triangulate(mesh);
            // Replace the old mesh
            node.setEntity(newMesh);
        }
        return true;
    }
});
MyDir = MyDir + RunExamples.getOutputFilePath("document.fbx");
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}
##  **Créer une scène de cube 3D**
Cette rubrique montre comment ajouter une géométrie de maillage à la scène 3D. L'exemple de code place un cube et enregistre la scène 3D dans les formats de fichier pris en charge.
###  **Créer un nœud cube**
Un nœud est invisible, mais la géométrie attachée au nœud peut être rendue.

{{% alert color="primary" %}} 

L'objet de classe Mesh est utilisé dans le code. Nous pouvons [Créer un objet de classe Mesh tel que raconté là-bas](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh).

{{% /alert %}} 

**Exemple:**

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize Node class object
Node cubeNode = new Node("cube");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the Mesh geometry
cubeNode.setEntity(mesh);
// Add Node to a scene
scene.getRootNode().getChildNodes().add(cubeNode);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("CubeScene.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}

{{% alert color="primary" %}} 

REMARQUE: Les entités attachées au nœud racine sont généralement ignorées dans les logiciels CAD/CAM, nous devons donc créer un nouveau nœud pour rendre la géométrie.

{{% /alert %}}
