---
title: Public API Changements dans Aspose.3D 1.5.0
type: docs
weight: 20
url: /fr/net/public-api-changes-in-aspose-3d-1-5-0/
---
**Résumé du contenu**

- [Convertissez le Primitif en Mesh et créez une scène à partir de modèles primitifs 3D](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [Convertir un maillage en maillage Triangle avec la disposition de mémoire personnalisée du Vertex](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [Maille fendue](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [Suppression du format Distreet3DS.](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [Ajoute le format Discreet3DS.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [Ajoute la propriété FlipCoordinateSystem dans la classe Aspose.ThreeD.Formats.Universal3DConfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.3D API de la version 1.4.0 à 1.5.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses du Aspose.3D.

{{% /alert %}} 
### **Convertissez le Primitif en Mesh et créez une scène à partir de modèles primitifs 3D**
**Diverses classes, méthodes et propriétés sont ajoutées**

- **Ajoute l'interface Aspose.ThreeD. Entités. ImeshConvertible.** 
-Toute classe qui implémente cette interface peut être convertie en maillage tout en exportant vers n'importe quel format de fichier 3D.
- **Ajoute la classe Aspose.ThreeD. Entités. Primitif.** 
-Il est dérivé de la classe Entity et également de la classe de base pour toutes les classes primitives.
- **Ajoute la classe Aspose.ThreeD. Entités. Boîte/Cylindre/Avion/Sphère/Torus.** 
-Ceux-ci peuvent être utilisés pour définir la scène avec des primitives simples. Les développeurs peuvent également les convertir automatiquement en maillage.

Les primaires comprennent bon nombre des objets les plus basiques et les plus utilisés comme la boîte, la sphère, le plan, le cylindre et le tore. Les développeurs peuvent également les convertir en maillage à des fins de modification. Ces sujets aident à illustrer comment le faire:[Convertir le Primitif en Maille](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models)Et[Convertir le Primitif en Maille](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
### **Convertir un maillage en maillage Triangle avec la disposition de mémoire personnalisée du Vertex**
**Diverses classes, méthodes et propriétés sont ajoutées**

- **Ajoute la classe Aspose.ThreeD. Entités. TriMesh/TriMesh<T>** 
-TriMesh/TriMesh<T>Contient la définition des maillages en triangle avec une disposition de mémoire personnalisée, ce qui est utile lorsque le développeur a besoin de convertir la scène à ses propres formats de fichier propriétaires ou lors du rendu.
- **Ajoute la structure Aspose.ThreeD. Services publics. FVector2/FVector3/FVector4** 
-Ces classes présentent des composants vectoriels dans le flotteur. Seuls quelques GPU modernes prennent en charge un vecteur de double précision, les types de flotteurs à une seule précision sont plus bien accueillis dans le monde du rendu en temps réel. Ces remplacements coexisteront avec le Vector2/Vector3/Vector4 original puisqu'ils jouent différents rôles dans Aspose.3D. La double précision est principalement utilisée pour stocker les données du modèle car elle a moins d'erreurs accumulées. La précision unique est principalement utilisée dans le rendu ou la conversion des formats de fichiers propriétaires de l'utilisateur, car elle offre une meilleure acceptation et de meilleures performances. Nous avons introduit cet ensemble de vecteurs dans Aspose.3D 1.5 car nous avons ajouté la prise en charge de la disposition des sommets personnalisés, où les vecteurs flottants seront fréquemment utilisés.
- **Ajoute la classe d'attribut Aspose.ThreeD. Utilitaires. Semantil'attribut** 
-Le développeur peut définir une structure personnalisée pour le sommet et utiliser cet attribut pour marquer la sémantique des champs.
- **Ajoute la classe Aspose.ThreeD. Services publics. VertexDeclaration** 
-Il décrit la disposition de la mémoire du sommet.
- **Ajoute enum Aspose.ThreeD. Utilitaires. VertexFieldDataType/VertexFieldSemantic** 
-Ces types enum annotent respectivement le type de données et la sémantique du champ du sommet.
- **Ajoute la classe Aspose.ThreeD. Utilitaires. VertexField** 
-Il décrit chaque champ dans la disposition de mémoire personnalisée de Vertex.
- **Ajoute la classe Aspose.ThreeD. Utilitaires. Vertex** 
-Il peut être utilisé pour accéder au sommet brut dans TriMesh/TriMesh<T>

Les développeurs peuvent convertir n'importe quel objet maillé en maillage triangulaire avec la disposition de mémoire personnalisée du sommet. Les progiciels graphiques et les périphériques matériels fonctionnent plus efficacement sur des triangles. Ce sujet d'aide illustre comment le faire:[Convertir un maillage en maillage Triangle avec la disposition de mémoire personnalisée du Vertex](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
### **Maille fendue**
**Diverses classes, méthodes et propriétés sont ajoutées**

- **Ajoute enum Aspose.ThreeD. Entités. SplitMeshPolicy** 
-Il spécifie la politique de données utilisée dans l'algorithme de division du maillage, nous prenons en charge deux politiques, partageons des données entre des sous-maillages ou chaque sous-maillage a ses propres données (données utilisées uniquement).
- **Ajoute 3 méthodes SplitMesh à Aspose.ThreeD. Entités. Classe de polygonmodificateur** 
1. Divisez les mailles d'un nœud spécifié en sous-maillages par définition du matériau.
1. Divisez tous les maillages de la scène donnée en sous-maillages par définition matérielle.
1. Divisez le maillage donné en sous-mailles par définition du matériau.
- **Ajoute la propriété FlipCoordinateSystem dans la classe Aspose.ThreeD.Formats.Universal3DConfig** 
-Il permet aux utilisateurs de retourner le système de coordonnées de U3D pendant l'importation ou l'exportation.

Les développeurs peuvent exiger de diviser automatiquement un maillage par matériau, de sorte que chaque maillage n'utilise qu'un seul matériau ou un maillage divisé en spécifiant le matériau. Ces sujets aident à illustrer comment le faire:[Diviser un maillage en spécifiant le matériau](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial)Et[Divisez tous les mailles d'une scène par matériau](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
### **Suppression du format Distreet3DS.**
Le format Distreet3DS est marqué comme obsolète en raison du sort incorrect.
### **Ajoute le format Discreet3DS.**
Le format Discreet3DS a été introduit.
### **Ajoute la propriété FlipCoordinateSystem dans la classe Aspose.ThreeD.Formats.Universal3DConfig**
Il permet aux utilisateurs de retourner le système de coordonnées du U3D pendant l'importation ou l'exportation.
