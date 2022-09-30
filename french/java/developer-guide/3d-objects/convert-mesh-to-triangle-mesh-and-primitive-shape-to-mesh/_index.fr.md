---
title: Convertir la maille en maille triangulaire et la forme primitive en maille
type: docs
weight: 20
url: /fr/java/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for Java API a un support pour convertir le maillage en maillage triangulaire avec une disposition de mémoire personnalisée du sommet. La disposition de la mémoire personnalisée du Vertex est définie dynamiquement par la classe VertexDeclaration dans les exemples de code.
---
## **Convertir Mesh en Triangle Mesh avec une disposition de mémoire personnalisée de Vertex**
Aspose.3D for Java API a un support pour convertir le maillage en maillage triangulaire avec une disposition de mémoire personnalisée du sommet. La disposition de la mémoire personnalisée du Vertex est définie dynamiquement par la classe `VertexDeclaration` dans les exemples de code.

{{% alert color="primary" %}}

Ce sujet d'aide crée des maillages à partir de la boîte et de la sphère pour garder le code complet et court. Les développeurs peuvent construire un maillage manuellement comme raconté dans ce sujet d'aide:[Créer 3D Maille Cube](/3d/fr/java/create-3d-mesh-and-scene/).

{{% /alert %}}

Les développeurs peuvent convertir le maillage en maillage triangulaire car toute structure complexe (surface) peut être représentée comme un tas de triangles. Le triangle est la géométrie la plus atomique. Ainsi, il est utilisé comme base pour presque tout. Cet exemple de code convertit une boîte en maillage triangle avec une disposition de mémoire personnalisée.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.java" >}}
## **Convertir Forme primitive en Maille**
Aspose.3D for Java API a l'appui de convertir toute forme primitive en maillage. Les formes primitives comprennent la plupart des objets les plus basiques et les plus utilisés comme la boîte, la sphère, le plan, le cylindre et le tore.

{{% alert color="primary" %}}

Toute classe qui implémente une interface ImeshConvertible peut être convertie en maillage lors de l'exportation vers n'importe quel format de fichier 3D.

{{% /alert %}}
### **Convertir Sphère primitive en Maille**
Une sphère est un objet géométrique parfaitement rond dans un espace tridimensionnel qui apparaît partout, des balles de sport aux planètes dans l'espace. Utilisons la Sphère primitive pour créer un maillage.
L'exemple de code ci-dessous convertit une sphère en maillage.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertSpherePrimitivetoMesh.java" >}}
### **Convertir la boîte en maille**
Une boîte décrit une variété de conteneurs et de récipients pour une utilisation permanente comme stockage, ou pour une utilisation temporaire, souvent pour le transport du contenu. Utilisons la boîte primitive pour créer un maillage. L'exemple de code ci-dessous convertit une boîte en maillage.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertBoxPrimitivetoMesh.java" >}}
### **Convertir un avion en maillage**
Un plan s'étend infiniment sans épaisseur. Un exemple de plan est un plan de coordonnées. Permet d'utiliser le plan primitif pour créer un maillage. L'exemple de code ci-dessous convertit un plan en maillage.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertPlanePrimitivetoMesh.java" >}}
### **Convertir un cylindre en maille**
Un cylindre est l'une des formes géométriques curvilignes les plus élémentaires, la surface formée par les points à une distance fixe d'une ligne droite donnée, l'axe du cylindre. Il peut être utilisé dans de nombreux endroits, par exemple comme pilier devant une maison ou comme arbre de transmission de voiture. Permet d'utiliser le cylindre primitif pour créer un maillage. L'exemple de code ci-dessous convertit un cylindre en maillage.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertCylinderPrimitivetoMesh.java" >}}
### **Convertir un Torus en Maille**
Un tore est une surface de révolution générée en faisant tourner un cercle dans un espace tridimensionnel autour d'un axe coplanaire avec le cercle. Si l'axe de révolution ne touche pas le cercle, la surface a une forme d'anneau et s'appelle un tore de révolution. Utilisons le Torus primitif pour créer un maillage. L'exemple de code ci-dessous convertit un Torus en maillage.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertTorusPrimitivetoMesh.java" >}}
