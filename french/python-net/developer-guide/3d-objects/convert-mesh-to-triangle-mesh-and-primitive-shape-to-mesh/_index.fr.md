---
title: Convertir la maille en maille triangulaire et la forme primitive en maille
type: docs
weight: 30
url: /fr/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D pour Python via .NET API permet aux développeurs de convertir n'importe quel objet maillé en maillage triangulaire avec une disposition de mémoire personnalisée du sommet. La disposition de la mémoire personnalisée du Vertex est définie à l'aide du Struct ou dynamiquement par la classe VertexDeclaration dans les exemples de code.
---
## **Convertir un maillage en maillage Triangle avec la disposition de mémoire personnalisée du Vertex**
[Aspose.3D pour Python via .NET](https://products.aspose.com/3d/python-net/)API permet aux développeurs de convertir n'importe quel objet maillé en maillage triangulaire avec une disposition de mémoire personnalisée du sommet. La disposition de la mémoire personnalisée du Vertex est définie à l'aide du Struct ou dynamiquement par la classe [`VertexDeclaration`](http://www.aspose.com/api/net/3d/aspose.threed.utilities/vertexdeclaration) dans les exemples de code.

{{% alert color="primary" %}}

Ce sujet d'aide crée des maillages à partir de la boîte et de la sphère pour garder le code complet et court. Les développeurs peuvent construire un maillage manuellement comme raconté dans ce sujet d'aide:[Créer un maillage Cube 3D](/3d/fr/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Ces exemples montrent comment:

- [Convertir une sphère en maille triangle avec une disposition de mémoire personnalisée du sommet (défini dans le Struct)](/3d/fr/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convertir une boîte en Triangle Mesh avec une disposition de mémoire personnalisée du sommet (définie par la classe VertexDeclaration)](/3d/fr/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
### **Convertir Maille**
Les développeurs peuvent convertir le maillage en maillage triangulaire car toute structure complexe (surface) peut être représentée comme un tas de triangles. Le triangle est la géométrie la plus atomique. Ainsi, il est utilisé comme base pour presque tout.
### **Les sommets d'accès d'un maillage Triangle**
Les développeurs peuvent accéder aux indices, aux sommets réels, aux sommets avant la fusion et au total des octets de sommets en mémoire.

L'exemple ci-dessous convertit une sphère en maillage triangle avec une disposition de mémoire personnalisée.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.py" >}}




Ci-dessous, l'exemple convertit une boîte en maillage triangle avec une disposition de mémoire personnalisée.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.py" >}}
## **Convertissez le 'Primitive' en un 'Mesh'**
En utilisant Aspose.3D pour Python via .NET, les développeurs peuvent convertir n'importe quel objet primitif en maillage. Les primaires comprennent bon nombre des objets les plus basiques et les plus utilisés comme la boîte, la sphère, le plan, le cylindre et le tore.

{{% alert color="primary" %}}

Toute classe qui implémente une interface ImeshConvertible peut être convertie en maillage lors de l'exportation vers n'importe quel format de fichier 3D.

{{% /alert %}}
### **Convertir un 'sphère' en 'mesh'**
Une sphère est un objet géométrique parfaitement rond dans un espace tridimensionnel qui apparaît partout, des balles de sport aux planètes dans l'espace. Utilisons la Sphère primitive pour créer un maillage.
L'exemple de code ci-dessous convertit une sphère en maillage.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSpherePrimitivetoMesh-ConvertSpherePrimitivetoMesh.py" >}}
### **Convertir une «boîte» en «mesh»**
Une boîte décrit une variété de conteneurs et de récipients pour une utilisation permanente comme stockage, ou pour une utilisation temporaire, souvent pour le transport du contenu. Utilisons la boîte primitive pour créer un maillage. L'exemple de code ci-dessous convertit une boîte en maillage.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxPrimitivetoMesh-ConvertBoxPrimitivetoMesh.py" >}}
### **Convertir un «avion» en «mesh»**
Un plan s'étend infiniment sans épaisseur. Un exemple de plan est un plan de coordonnées. Permet d'utiliser le plan primitif pour créer un maillage. L'exemple de code ci-dessous convertit un plan en maillage.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertPlanePrimitivetoMesh-ConvertPlanePrimitivetoMesh.py" >}}
### **Convertir un 'cylindre 'en 'mesh'**
Un cylindre est l'une des formes géométriques curvilignes les plus élémentaires, la surface formée par les points à une distance fixe d'une ligne droite donnée, l'axe du cylindre. Il peut être utilisé dans de nombreux endroits, par exemple comme pilier devant une maison ou comme arbre de transmission de voiture. Permet d'utiliser le cylindre primitif pour créer un maillage. L'exemple de code ci-dessous convertit un cylindre en maillage.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertCylinderPrimitivetoMesh-ConvertCylinderPrimitivetoMesh.py" >}}
### **Convertir un 'Torus' en 'Mesh'**
Un tore est une surface de révolution générée en faisant tourner un cercle dans un espace tridimensionnel autour d'un axe coplanaire avec le cercle. Si l'axe de révolution ne touche pas le cercle, la surface a une forme d'anneau et s'appelle un tore de révolution. Utilisons le Torus primitif pour créer un maillage. L'exemple de code ci-dessous convertit un Torus en maillage.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertTorusPrimitivetoMesh-ConvertTorusPrimitivetoMesh.py" >}}
