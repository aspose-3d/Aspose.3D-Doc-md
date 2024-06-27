---
title: Public API Changements dans Aspose.3D 1.5.0
type: docs
weight: 20
url: /fr/net/public-api-changes-in-aspose-3d-1-5-0/
---
**Résumé du contenu**

- [Convertir la primitive en un maillage et créer une scène à partir de modèles primitifs 3D](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [Convertir un maillage en maillage Triangle avec la disposition de mémoire personnalisée du Vertex](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [Maille fendue](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [Suppression du format Distreet3DS.](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [Ajoute le format Discreet3DS.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [Ajoute la propriété FlipCoordinateSystem dans la classe Aspose.ThreeD.Formats.Universal3DConfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

Ce document décrit les changements apportés à Aspose.3D API de la version 1.4.0 à 1.5.0, qui peuvent intéresser les développeurs de modules/applications. Il inclut non seulement des méthodes publiques nouvelles et mises à jour, mais aussi une description de tout changement de comportement dans les coulisses de Aspose.3D.

{{% /alert %}} 
###  **Convertir la primitive en un maillage et créer une scène à partir de modèles primitifs 3D**
**Diverses classes, méthodes et propriétés sont ajoutées**

- **Ajoute l'interface Aspose.ThreeD.Entities.IMeshConvertible.** 
Toute classe qui implémente cette interface peut être convertie en maillage lors de l'exportation vers n'importe quel format de fichier 3D.
- **Ajoute la classe Aspose.ThreeD.Entities.Primitive.** 
-Il est dérivé de la classe Entity et également de la classe de base pour toutes les classes primitives.
- **Ajoute la classe Aspose.ThreeD.Entities.Box/Cylindre/Plan/Sphère/Torus.** 
-Ceux-ci peuvent être utilisés pour définir la scène avec des primitives simples. Les développeurs peuvent également les convertir automatiquement en maillage.

Les primitives comprennent plusieurs des objets les plus basiques et les plus utilisés comme la boîte, la sphère, le plan, le cylindre et le tore. Les développeurs peuvent également les convertir en maillage à des fins de modification. Ces rubriques d'aide illustrent comment procéder: [Convertir le Primitif en Maille](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models) et [Convertir le Primitif en Maille](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
###  **Convertir un maillage en maillage Triangle avec la disposition de mémoire personnalisée du Vertex**
**Diverses classes, méthodes et propriétés sont ajoutées**

- **Ajoute la classe Aspose.ThreeD.Entities.TriMesh/TriMesh<T>** 
-TriMesh/TriMesh<T>Contient la définition des maillages en triangle avec une disposition de mémoire personnalisée, ce qui est utile lorsque le développeur a besoin de convertir la scène à ses propres formats de fichier propriétaires ou lors du rendu.
- **Ajoute la structure Aspose.ThreeD.Utilities.FVector2/FVector3/FVector4** 
-Ces classes présentent des composants vectoriels dans le float. Seuls quelques GPU modernes prend en charge le vecteur de double précision, les types de flotteur de simple précision sont plus bien accueillis dans le monde de rendu en temps réel. Ces remplacements coexisteront avec le Vector2/Vector3/Vector4 d'origine car ils jouent des rôles différents dans Aspose.3D. Double précision est principalement utilisé pour stocker les données du modèle, car il a moins d'erreurs accumulées. Single-précision est principalement utilisé dans le rendu ou la conversion de formats de fichiers propriétaires de l'utilisateur, car il a une meilleure acceptation et performance. Nous avons introduit cet ensemble de vecteurs dans Aspose.3D 1.5 parce que nous avons ajouté la prise en charge de la disposition des sommets personnalisés, où les vecteurs flottants seront fréquemment utilisés.
- **Ajoute la classe d'attribut Aspose.ThreeD.Utilities.SemanticAttribute** 
-Le développeur peut définir une structure personnalisée pour le sommet et utiliser cet attribut pour marquer la sémantique des champs.
- **Ajoute la classe Aspose.ThreeD.Utilities.VertexDeclaration** 
-Il décrit la disposition de la mémoire du sommet.
- **Ajoute enum Aspose.ThreeD.Utilities.VertexFieldDataType/VertexFieldSemantic** 
-Ces types enum annotent respectivement le type de données et la sémantique du champ du sommet.
- **Ajoute la classe Aspose.ThreeD.Utilities.VertexField** 
-Il décrit chaque champ dans la disposition de mémoire personnalisée de Vertex.
- **Ajoute la classe Aspose.ThreeD.Utilities.Vertex** 
-Il peut être utilisé pour accéder au sommet brut dans TriMesh/TriMesh<T>

Les développeurs peuvent convertir n'importe quel objet de maillage au maillage triangulaire avec la disposition de mémoire personnalisée du sommet. Les progiciels graphiques et les dispositifs matériels fonctionnent plus efficacement sur des triangles. Cette rubrique d'aide illustre comment procéder: [Convertir un maillage en maillage Triangle avec la disposition de mémoire personnalisée du Vertex](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
###  **Maille fendue**
**Diverses classes, méthodes et propriétés sont ajoutées**

- **Ajoute enum Aspose.ThreeD.Entities.SplitMeshPolicy** 
-Il spécifie la politique de données utilisée dans l'algorithme de division du maillage, nous prenons en charge deux politiques, partageons des données entre des sous-maillages ou chaque sous-maillage a ses propres données (données utilisées uniquement).
- **Ajoute 3 méthodes SplitMesh à la classe Aspose.ThreeD.Entities.PolygonModifier** 
1. Divisez les mailles d'un nœud spécifié en sous-maillages par définition du matériau.
1. Divisez tous les maillages de la scène donnée en sous-maillages par définition matérielle.
1. Divisez le maillage donné en sous-mailles par définition du matériau.
- **Ajoute la propriété FlipCoordinateSystem dans la classe Aspose.ThreeD.Formats.Universal3DConfig** 
Il permet aux utilisateurs de retourner le système de coordonnées de U3D pendant l'importation ou l'exportation.

Les développeurs peuvent exiger de diviser automatiquement un maillage par matériau, de sorte que chaque maillage utilise uniquement un matériau ou un maillage divisé en spécifiant le matériau. Ces rubriques d'aide illustrent comment procéder: [Diviser un maillage en spécifiant le matériau](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial) et [Divisez tous les mailles d'une scène par matériau](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
###  **Suppression du format Distreet3DS.**
Le format Distreet3DS est marqué comme obsolète en raison du sort incorrect.
###  **Ajoute le format Discreet3DS.**
Le format Discreet3DS a été introduit.
###  **Ajoute la propriété FlipCoordinateSystem dans la classe Aspose.ThreeD.Formats.Universal3DConfig**
Il permet aux utilisateurs de retourner le système de coordonnées de U3D pendant l'importation ou l'exportation.
