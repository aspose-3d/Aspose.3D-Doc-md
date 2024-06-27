---
title: MappingMode et ReferenceMode explique
type: docs
weight: 10
url: /fr/net/mapping-mode-and-reference-mode-explains
description: En utilisant Aspose.3D for .NET, les développeurs peuvent définir un maillage avec divers éléments de données de sommet, ici nous expliquons comment mapper les données au composant de maillage et resuze les données.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/), les développeurs peuvent définir des maillages avec divers éléments de données de sommet, y compris des normales, des couleurs et des poids. Aspose.3D offre deux mécanismes pour optimiser la réutilisation des données: `MappingMode` et `ReferenceMode`. Ces mécanismes sont conçus pour minimiser l'empreinte mémoire des maillages, en particulier dans les formats avancés comme FBX et USD. MappingMode permet un mappage efficace des données de sommet vers les composants de maillage, tandis que ReferenceMode facilite le référencement des données d'éléments de sommet sur plusieurs composants de maillage. Ensemble, ces fonctionnalités améliorent les performances et l'efficacité de la mémoire, faisant de Aspose.3D un outil puissant pour gérer des modèles complexes 3D dans des applications .NET.

{{% /alert %}}



###  `MappingMode` explique

 `MappingMode` détermine comment les données de l'élément sont mappées à la surface de la géométrie dans Aspose.3D for .NET. Il fournit diverses façons de définir cette cartographie:

1. **ControlPoint**Chaque élément de données est mappé au point de contrôle de la géométrie. Ce mode garantit que chaque point de contrôle, qui définit la forme de la géométrie, est associé à une donnée spécifique.
1. **PolygonVertex**Les données sont mappées au sommet d'un polygone. Dans les cas où un point de contrôle est partagé par plusieurs polygones, chaque instance du point de contrôle, telle qu'elle apparaît dans différents polygones, aura ses propres données distinctes. Cela garantit que même les points de contrôle partagés peuvent avoir des données uniques lorsqu'ils servent de sommets pour différents polygones.
1. **Polygone**Les données sont mappées à l'ensemble du polygone. Cela signifie que tous les sommets d'un polygone partagent le même élément de données. Ce mode est utile lorsque des données uniformes doivent être appliquées sur toute la surface du polygone, ce qui garantit la cohérence au sein du polygone.
1. **Bord**, Les données sont mappées aux bords de la géométrie. Chaque point d'extrémité d'une arête partage les mêmes données, ce qui permet d'appliquer des données uniformes aux arêtes tout en permettant des données distinctes pour différentes arêtes. Cela peut être particulièrement utile pour définir des caractéristiques spécifiques aux arêtes, telles que les valeurs de pli ou les attributs basés sur les arêtes.
1. **AllSame**Un seul élément de données est mappé sur toute la surface de la géométrie. Que les données soient interprétées comme des points de contrôle, des sommets de polygone ou des extrémités d'arête, la même valeur de données est appliquée uniformément sur tous les éléments. Ce mode est idéal pour les scénarios où une valeur constante doit être maintenue dans toute la géométrie, assurant un attribut uniforme sur l'ensemble du modèle 3D.




###  `ReferenceMode` explique
 `ReferenceMode` définit s'il faut réutiliser les données par des indices, il y a trois politiques pour `ReferenceMode`:

1.**Directement**, Les données sont directement référencées et stockées dans la propriété `Data` de `VertexElement`.
1.**IndexToDirect**, Les données sont référencées par index, puis accédées par index dans la liste de données de `VertexElement`.
1.**Index**, Les données ne sont référencées que par index, maintenant seul le `VertexElementMaterial` utilise ce mode de référence, c'est similaire à `IndexToDirect` mais les différences sont que les matériaux sont définis sous la propriété `Materials` de `Node`, pas dans le `VertexElementMaterial`, tout `VertexElement` ne fonctionne qu'avec des données primitives.



Par exemple, étant donné une définition d'un cube:

{{< highlight "csharp" >}}
var cube = new Mesh();
Vector4[] controlPoints = new Vector4[]
{
    new Vector4( -5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 10.0, -5.0, 1.0),
    new Vector4( -5.0, 10.0, -5.0, 1.0)
};
cube.ControlPoints.AddRange(controlPoints);

// Front face (Z+)
cube.CreatePolygon(new int[] { 0, 1, 2, 3 });
// Right side (X+)
cube.CreatePolygon(new int[] { 1, 5, 6, 2 });
// Back face (Z-)
cube.CreatePolygon(new int[] { 5, 4, 7, 6 });
// Left side (X-)
cube.CreatePolygon(new int[] { 4, 0, 3, 7 });
// Bottom face (Y-)
cube.CreatePolygon(new int[] { 0, 4, 5, 1 });
// Top face (Y+)
cube.CreatePolygon(new int[] { 3, 2, 6, 7 });

var vertexColor = (VertexElementVertexColor) cube.CreateElement(VertexElementType.VertexColor);
vertexColor.MappingMode = MappingMode.ControlPoint;
var red = new Vector4(1, 0, 0, 1);
var green = new Vector4(0, 1, 0, 1);
var blue = new Vector4(0, 0, 1, 1);
var white = new Vector4(1, 1, 1, 1);

{{< /highlight >}}

Si vous souhaitez assigner le rouge aux points de contrôle 0 et 1, le vert aux points de contrôle 2 et 3, le bleu aux points de contrôle 4 et 5 et le blanc aux points de contrôle 6 et 7, vous pouvez le faire avec l'approche suivante:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.Direct;
vertexColor.Data.Add(red); // 0
vertexColor.Data.Add(red); // 1
vertexColor.Data.Add(green); // 2
vertexColor.Data.Add(green); // 3
vertexColor.Data.Add(blue); // 4
vertexColor.Data.Add(blue); // 5
vertexColor.Data.Add(white); // 6
vertexColor.Data.Add(white); // 7
{{< /highlight >}}

Pour attribuer efficacement des couleurs aux points de contrôle et réduire la consommation de mémoire, vous pouvez utiliser des indices pour référencer les couleurs. En définissant les couleurs séparément, puis en les référencant avec des indices, vous pouvez minimiser la redondance. Voici comment vous pouvez y parvenir:

Tout d'abord, définissez 4 couleurs dans le type Vector4 pour les couleurs uniques, puis utilisez un tableau de 8 indices pour attribuer ces couleurs à chaque point de contrôle:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.IndexToDirect;
vertexColor.Data.Add(red);
vertexColor.Data.Add(green);
vertexColor.Data.Add(blue);
vertexColor.Data.Add(white);

vertexColor.SetIndices(new int[] { 0, 0, 1, 1, 2, 2, 3, 3 });
{{< /highlight >}}

Dans cette approche:

1. Définir des couleurs uniques: Seules 4 couleurs sont définies (rouge, vert, bleu, blanc) en tant qu'instances Vector4.
1. Créer un tableau d'index de couleur: Un tableau de 8 indices est utilisé pour référencer ces 4 couleurs pour chaque point de contrôle.
1. Mappage des couleurs à l'aide d'indices: en référençant les couleurs par le biais d'indices, vous réduisez la consommation de mémoire, car chaque couleur est stockée une fois et réutilisée sur plusieurs points de contrôle.

Cette méthode optimise l'utilisation de la mémoire en réduisant le stockage de données redondantes, ce qui rend votre modèle 3D plus efficace.