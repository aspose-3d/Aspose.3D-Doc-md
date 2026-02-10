---
title: Convertir la maille en maille triangulaire et la forme primitive en maille
type: docs
weight: 20
url: /fr/java/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for Java API a le support pour convertir le maillage en maillage triangulaire avec la disposition de mémoire personnalisée du sommet. La disposition mémoire personnalisée du sommet est définie dynamiquement par la classe VertexDeclaration dans les exemples de code.
---
##  **Convertir Mesh en Triangle Mesh avec une disposition de mémoire personnalisée de Vertex**
Aspose.3D for Java API a le support pour convertir le maillage en maillage triangulaire avec la disposition de mémoire personnalisée du sommet. La disposition de mémoire personnalisée du sommet est définie dynamiquement par la classe `VertexDeclaration` dans les exemples de code.

{{% alert color="primary" %}}

Cette rubrique d'aide crée des maillages à partir de la boîte et de la sphère pour garder le code complet et court. Les développeurs peuvent construire un maillage manuellement comme rapporté dans cette rubrique d'aide: [Créer 3D Cube Mesh](/3d/fr/java/create-3d-mesh-and-scene/).

{{% /alert %}}

Les développeurs peuvent convertir le maillage en maillage triangulaire car toute structure complexe (surface) peut être représentée comme un tas de triangles. Le triangle est la géométrie la plus atomique. Ainsi, il est utilisé comme base pour presque tout. Cet exemple de code convertit une boîte en maillage triangle avec une disposition de mémoire personnalisée.



{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize Node class object
Node cubeNode = new Node("box");
// Get mesh of the Box
Mesh box = (new Box()).toMesh();
// Create a customized vertex layout
VertexDeclaration vd = new VertexDeclaration();
VertexField position = vd.addField(VertexFieldDataType.F_VECTOR4, VertexFieldSemantic.POSITION);
vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.NORMAL);
// Get a triangle mesh
TriMesh triMesh = TriMesh.fromMesh(box);
// ExEnd:ConvertBoxMeshtoTriangleMeshCustomMemoryLayout
// Point node to the Mesh geometry
cubeNode.setEntity(box);
// Add Node to a scene
scene.getRootNode().getChildNodes().add(cubeNode);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir() + RunExamples.getOutputFilePath("BoxToTriangleMeshCustomMemoryLayoutScene.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}
##  **Convertir Forme primitive en Maille**
Aspose.3D for Java API a le support de convertir n'importe quelle forme primitive en maillage. Les formes primitives comprennent la plupart des objets basiques et utilisés comme boîte, sphère, plan, cylindre et tore.

{{% alert color="primary" %}}

Toute classe qui implémente une interface IMeshConvertible peut être convertie en maillage lors de l'exportation vers n'importe quel format de fichier 3D.

{{% /alert %}}
###  **Convertir Sphère primitive en Maille**
Une sphère est un objet géométrique parfaitement rond dans un espace tridimensionnel qui apparaît partout, des balles de sport aux planètes dans l'espace. Utilisons la Sphère primitive pour créer un maillage.
L'exemple de code ci-dessous convertit une sphère en maillage.

{{< highlight "java" >}}
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
// Convert a Sphere to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convertir la boîte en maille**
Une boîte décrit une variété de conteneurs et de récipients pour une utilisation permanente comme stockage, ou pour une utilisation temporaire, souvent pour le transport du contenu. Utilisons la boîte primitive pour créer un maillage. L'exemple de code ci-dessous convertit une boîte en maillage.

{{< highlight "java" >}}
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convertir un avion en maillage**
Un plan s'étend infiniment sans épaisseur. Un exemple de plan est un plan de coordonnées. Permet d'utiliser le plan primitif pour créer un maillage. L'exemple de code ci-dessous convertit un plan en maillage.

{{< highlight "java" >}}
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
// Convert a Plane to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convertir un cylindre en maille**
Un cylindre est l'une des formes géométriques curvilignes les plus élémentaires, la surface formée par les points à une distance fixe d'une ligne droite donnée, l'axe du cylindre. Il peut être utilisé dans de nombreux endroits, par exemple comme pilier devant une maison ou comme arbre de transmission de voiture. Permet d'utiliser le cylindre primitif pour créer un maillage. L'exemple de code ci-dessous convertit un cylindre en maillage.

{{< highlight "java" >}}
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
// Convert a Cylinder to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convertir un Torus en Maille**
Un tore est une surface de révolution générée en faisant tourner un cercle dans un espace tridimensionnel autour d'un axe coplanaire avec le cercle. Si l'axe de révolution ne touche pas le cercle, la surface a une forme d'anneau et s'appelle un tore de révolution. Utilisons le Torus primitif pour créer un maillage. L'exemple de code ci-dessous convertit un Torus en maillage.

{{< highlight "java" >}}
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
// Convert a Torus to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
