---
title: Aspose.3D Modèle objet de document (DOM)
type: docs
weight: 20
url: /fr/java/aspose-3d-document-object-model
description: Chaque scène 3D peut comprendre n'importe quel nombre de vues. En utilisant Aspose.3D for Java API, les développeurs peuvent capturer un ou plusieurs viewports dans une seule capture d'écran. Ils peuvent le rendre dans l'application Java basée sur GUI ou une image.
---
Le Aspose.3D Document Object Model (DOM) est une représentation puissante en mémoire d'une scène 3D. Il offre aux développeurs la possibilité de lire, manipuler et modifier le contenu et le formatage d'une scène 3D par programmation.

Dans cette section, nous allons explorer les classes clés du DOM Aspose.3D et leurs relations. En utilisant ces classes, vous pouvez obtenir un accès par programmation à divers éléments d'une scène 3D.

Plongeons dans les classes principales du DOM Aspose.3D:

* **Scène**La classe Scene représente la racine de la hiérarchie de scène 3D. Il sert de conteneur pour tous les autres éléments et fournit des méthodes pour manipuler la scène globale.
* **Nœud**Les nœuds sont les blocs de construction d'une scène 3D. Ils représentent des objets individuels ou des entités au sein de la scène, tels que des maillages, des lumières, des caméras ou des groupes. Les nœuds peuvent être transformés, animés et texturés.
* **Entités**Les classes Entities englobent un large éventail d'objets et d'éléments qui composent une scène 3D. Il comprend des entités telles que des maillages, des lumières, des caméras, des profils, etc. Ces entités servent de blocs de construction, vous permettant de créer des scènes complexes en les combinant et en les manipulant par programmation. La catégorie Entités fournit l'accès et le contrôle sur ces éléments fondamentaux d'une scène 3D.
* **Matériaux**Les classes Materials s'articulent autour de la définition des propriétés visuelles des objets dans une scène 3D. Il fournit des outils pour créer, modifier et contrôler par programmation des matériaux, qui déterminent comment la lumière interagit avec les surfaces. En ajustant des propriétés telles que la couleur, la texture, la transparence et la réflexion, vous pouvez obtenir divers effets visuels et personnaliser l'apparence de vos modèles 3D.
* **Animations**Les classes d'animation se concentrent sur la création et le contrôle des mouvements et des transformations dans une scène 3D. Il vous permet de définir et de manipuler des animations par programmation, permettant aux objets de se déplacer, de faire pivoter, de mettre à l'échelle ou de modifier des propriétés au fil du temps. Avec cette catégorie, vous pouvez apporter des éléments dynamiques et interactifs à vos scènes 3D.

En utilisant les classes DOM Aspose.3D mentionnées ci-dessus, vous pouvez interagir par programmation avec et manipuler le contenu et la structure d'une scène 3D. Cela offre flexibilité et contrôle lorsque vous travaillez avec des modèles 3D dans vos applications.


## Structure de la scène

Lorsque Aspose.3D lit un fichier 3D en mémoire, il génère des objets de différents types pour représenter les différents éléments de la scène 3D.


La structure de scène dans Aspose.3D suit le modèle de conception composite, qui offre flexibilité et organisation:

 * Les nœuds servent de conteneurs pouvant contenir d'autres nœuds, ce qui permet de regrouper différents objets dans la scène.
 * Chaque nœud peut avoir sa propre transformation, qui s'applique également à ses nœuds enfants.
 * Tous les types d'entités spatiales dans Aspose.3D doivent être placés sous une instance de nœud. Cela garantit que les objets tels que les maillages, les lumières, les caméras et d'autres éléments sont organisés dans la hiérarchie de la scène.
 * Les nœuds peuvent contenir plusieurs matériaux, et la relation entre les polygones et les matériaux attachés à un nœud est traitée à l'aide du concept `VertexElementMaterial` dans l'objet Mesh.


! [Hiérarchie de la scène](scene.png)


## Entités spatiales
Toutes les entités spatiales dans Aspose.3D héritent de la classe `Entity`, servant de blocs de construction fondamentaux pour la construction d'environnements virtuels. Aspose.3D catégorise ces entités en plusieurs grandes catégories, chacune ayant son propre but et sa propre fonctionnalité.

! [Entités](entity.png)

* **Primitif**La classe `Primitive` sert de classe de base pour toutes les géométries procédurales 3D dans Aspose.3D, telles que `Cylinder`, `Torus` et `Sphere`. Ces géométries peuvent être définies en utilisant un ensemble minimal de paramètres, ce qui facilite la création de formes 3D basiques.
* **Géométrie**Les géométries dans Aspose.3D sont généralement constituées de sommets, d'arêtes et de polygones qui définissent la forme et la structure d'un objet 3D. Cette catégorie englobe un large éventail de géométries complexes utilisées pour représenter divers objets au sein d'une scène 3D.
* **Profil**Les profils, similaires aux primitives, définissent des contours fermés 2D dans le plan x-y. Ils fournissent un moyen de créer des formes 2D qui peuvent être extrudées pour générer des géométries 3D correspondantes. Les profils sont souvent utilisés comme point de départ pour créer des objets 3D plus complexes.
* **Courbe**Contrairement aux profils, les courbes peuvent être ouvertes ou non connectées. Ils sont utilisés pour définir des chemins spatiaux dans 3D. Les courbes fournissent un moyen de créer des chemins flexibles et personnalisables que les objets peuvent suivre dans un environnement 3D.
* **Extrusion**Les extrusions sont une technique procédurale utilisée pour construire des géométries 3D en utilisant des profils et des courbes. En appliquant une extrusion à un profil ou à une courbe, une forme 3D peut être générée en étendant le profil ou la courbe le long d'une direction spécifiée. Cette approche permet de créer des géométries plus complexes et dynamiques.
* **Frustum**La catégorie de frustum inclut des objets tels que des lumières et des caméras. Les frustums définissent le volume d'affichage et la perspective dans une scène 3D. Les caméras utilisent des frustums pour déterminer la partie de la scène qui sera visible, tandis que les lumières utilisent des frustums pour définir la région dans laquelle elles éclairent la scène.

Ces catégories d'entités majeures dans Aspose.3D englobent une variété d'entités qui jouent un rôle essentiel dans la construction et la représentation d'environnements virtuels, fournissant une boîte à outils polyvalente pour créer et manipuler des scènes 3D.


### Types de géométrie

! [Types de géométrie](geometries.png)

Aspose.3D contient de nombreux types de géométrie:


* `Mesh` Maillage de polygone convivial pour l'outil de création.
* `PointCloud` Nuage de points.
* `NurbsSurface` Rational non uniforme B-Surfaces splines.
* `Patch` Surface définie par un ensemble de points de contrôle et de fonctions de fusion.
* `TriMesh` Rendre API-maillage basé sur un triangle convivial.


Les plus importants d'entre eux sont `Mesh` et `TriMesh`, les différences sont dans le tableau:

|Caractéristique| `Mesh` | `TriMesh` |
| ---     |---     |---        |
|Polygone sans triangle|Oui|Non|
|Facile à modifier|Oui|Non|
|Réutilisation de l'indice de données|Oui|Non|
|Cache CPU convivial|Non|Oui|
|Rendu API amical|Non|Oui|
|Mise en page de mémoire fixe|Non|Oui|

Les classes dérivées de `Geometry` sont conçues pour modifier et créer du contenu tandis que `TriMesh` est conçu pour le rendu.

Un `Geometry` se compose de points de contrôle et `VertexElement` qui a défini des données supplémentaires pour le point de contrôle/bord/polygone/polygone sommet, `Geometry` peut contenir zéro ou plus `VertexElement`, les sous-classes concrètes `Geometry` implémentaient différentes méthodes pour modéliser et représenter les géométries 3D.


! [Types de géométrie](mesh.png)


Vous pouvez créer manuellement un élément de sommet et lui attribuer des données. L'exemple de code suivant montre comment faire ceci:

{{< highlight "java" >}}
// Raw normal data
Vector4[] normals = new Vector4[]
{
    new Vector4(-0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258,-0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258,-0.577350258, 1.0)
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
VertexElementNormal elementNormal = (VertexElementNormal)mesh.createElement(VertexElementType.NORMAL, MappingMode.CONTROL_POINT, ReferenceMode.DIRECT);
// Copy the data to the vertex element
elementNormal.setData(normals);
{{< /highlight >}}

### Types de géométrie primitive


Aspose.3D fournit un ensemble de types de géométrie primitifs prédéfinis qui suivent des règles et des algorithmes spécifiques pour générer des modèles 3D. Ces types primitifs simplifient le processus de création de géométries 3D par rapport à l'utilisation de types Geometry plus complexes.

Les types primitifs prédéfinis disponibles dans Aspose.3D incluent:

*  `Box`: La primitive de boîte vous permet de créer des formes cuboïdes rectangulaires définies par leur largeur, leur hauteur et leur profondeur.
* Cylindre: Avec la primitive cylindre, vous pouvez générer des formes cylindriques en spécifiant le rayon et la hauteur. Ceci est utile pour créer des objets tels que des tubes ou des colonnes.
*  `Dish`: La primitive parabolique permet de créer des géométries en forme de parabole, couramment utilisées pour représenter des objets comme des bols ou des antennes paraboliques.
*  `Plane`: La primitive plane génère des surfaces planes définies par leur largeur et leur longueur. Il est fréquemment utilisé comme plan de fondation ou plan de masse dans les scènes 3D.
*  `Pyramid`: Avec la primitive pyramidale, vous pouvez créer des géométries en forme de pyramide caractérisées par leur taille de base et leur hauteur. Ceci est utile pour la construction d'objets tels que des bâtiments ou des pyramides.
*  `Torus`: La primitive de tore vous permet de générer des géométries en forme de beignet avec des rayons spécifiés pour les cercles majeurs et mineurs. Il convient à la création d'objets ressemblant à des anneaux ou à des pneus.
*  `RectangularTorus`: La primitive de tore rectangulaire produit des géométries de type tore avec des sections rectangulaires au lieu de circulaires. Il offre une flexibilité supplémentaire pour créer des formes uniques.
*  `Sphere`: La primitive de sphère génère des géométries parfaitement arrondies en fonction du rayon spécifié. C'est utile pour créer des objets comme des planètes ou des boules.

En utilisant ces types primitifs prédéfinis dans Aspose.3D, vous pouvez facilement créer une large gamme de géométries de base 3D. Cela simplifie le processus de modélisation et vous permet de façonner et d'assembler rapidement des objets dans vos scènes 3D.

! [Types de géométrie primitive](primitives.png)

L'exemple de code suivant montre comment créer une sphère avec un rayon spécifié:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java

        // initialize a scene
        Scene scene = new Scene();
        // initialize a Sphere
        Sphere sphere = new Sphere();
        // set radius
        sphere.setRadius(10);
        // add sphere to the scene
        scene.getRootNode().createChildNode(sphere);
        // save scene
        scene.save("sphere.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}


### Types d'extrusion

L'extrusion peut être utilisée pour créer une variété d'objets complexes 3D, c'est une méthode fondamentale dans la modélisation 3D qui consiste à étendre un profil 2D le long d'une courbe pour créer un objet 3D.

Dans Aspose.3D, nous avons fourni 3 types d'extrusion:

* `LinearExtrusion` L'extrusion linéaire prend un profil 2D en entrée et étend la forme dans la 3ème dimension.
* `RevolvedAreaSolid` Cette classe représente un modèle solide en tournant une section transversale fournie par un profil autour d'un axe.
* `SweptAreaSolid` Cette classe représente un modèle solide par un schéma de représentation de balayage permettant à une section transversale de profil 2D de balayer l'espace.


! [Extrusions](extrusions.png)

L'exemple de code suivant montre comment créer une extrusion linéaire à partir d'un profil de texte:

{{< highlight "java" >}}
    // Load font from bytes
    var font = FontFile.parse(Files.readAllBytes(Paths.get("test-font.otf")));
    // Create a Text profile
    var text = new Text();
    text.setFont(font);
    text.setContent("Hello World");
    text.setFontSize(10.0f);
    // Extrude the profile to give it a thickness.
    var linear = new LinearExtrusion(text, 10).toMesh();
    // create a scene from the mesh and save it to stl file
    var scene = new Scene(linear);
    scene.save("test.stl");


{{< /highlight >}}


### Types de courbe

Dans Aspose.3D, une courbe représente un ou plusieurs chemins spatiaux qui peuvent prendre diverses formes, telles que des lignes, des courbes NURBS ou des courbes composites composées de plusieurs segments de courbe. Les courbes sont couramment utilisées en conjonction avec les types d'extrusion pour créer des formes 3D dynamiques et complexes.

Les courbes peuvent être utilisées pour définir des chemins complexes que les objets suivent dans un environnement 3D, permettant des mouvements fluides et précis. En utilisant différents types de courbes et en les composant ensemble, vous pouvez obtenir des chemins spatiaux polyvalents et personnalisables pour vos modèles 3D.

De plus, certains formats de fichiers pris en charge par Aspose.3D offrent également la possibilité d'importer et d'exporter des données de courbe. Cela vous permet d'intégrer de manière transparente des courbes créées dans des applications externes ou de partager des courbes générées dans Aspose.3D avec d'autres logiciels.


! [Types de courbe](curves.png)

## Types de profil

Aspose.3D offre une gamme de profils 2D qui peuvent être utilisés pour créer des formes fermées ou des contours dans un environnement 3D. Ces profils permettent la création de structures 2D complexes qui peuvent être extrudées ou manipulées en géométries 3D. Voici quelques implémentations de profil notables dans Aspose.3D:

* `ParameterizedProfile`: Aspose.3D fournit plusieurs implémentations qui offrent des profils avec des formes standard. Ces profils prédéfinis permettent la création rapide de formes couramment utilisées telles que des cercles, des rectangles et des polygones.

* `MirroredProfile`: Ce type de profil vous permet de mettre en miroir un profil existant le long de l'axe Y, créant ainsi une forme symétrique. Il fournit un moyen pratique de générer des profils équilibrés et visuellement attrayants.

* `ArbitraryProfile`: avec l'implémentation de profil arbitraire, vous pouvez mapper une courbe arbitraire pour créer un profil fermé. Cela offre une flexibilité dans la conception de formes personnalisées en définissant une courbe et en la convertissant en un profil fermé pour une manipulation ultérieure.

* `Text`: Aspose.3D inclut la possibilité de générer des profils à partir du texte en utilisant une police spécifiée. Cette fonctionnalité vous permet de créer des profils sous forme de lettres, de chiffres ou de tout autre contenu textuel, en ajoutant un élément de personnalisation ou de branding à vos modèles 3D.

! [Types de profils 2D](profiles.png)

### Types de caméra et de lumière

! [Caméra et lumière](frustums.png)

## Types de matériaux

Aspose.3D fournit un support pour différents types de matériaux, y compris le matériau Lambert, le matériau Phong, le matériau PBR, le matériau spéculaire PBR et le matériau shader (uniquement disponible dans les fichiers FBX).

Chaque matériau dans Aspose.3D peut avoir différents attributs et propriétés qui définissent son apparence et son comportement dans une scène 3D. Ces matériaux peuvent être connectés à des instances de texture, ce qui améliore leurs caractéristiques visuelles.

Textures in Aspose.3D are associated with a specific material attribute. The texture type combines the parameter definitions for the image source and the texture sampler. By utilizing textures, you can apply detailed patterns, colors, and other visual effects to the surfaces of your 3D models.

Avec la prise en charge d'une gamme de types de matériaux et la possibilité de connecter des textures, Aspose.3D offre une flexibilité dans la création de matériaux visuellement attrayants et réalistes pour vos scènes 3D.

! [Types de matériaux](materials.png)

L'exemple de code suivant montre comment appliquer un matériau PBR à une géométrie:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// initialize a scene
Scene scene = new Scene();
// initialize PBR material object
PbrMaterial mat = new PbrMaterial();
// an almost metal material
mat.setMetallicFactor(0.9);
// material surface is very rough
mat.setRoughnessFactor(0.9);
// create a box to which the material will be applied
Node boxNode = scene.getRootNode().createChildNode("box", new Box());
boxNode.setMaterial(mat);
// save 3d scene into USDZ format
scene.save(MyDir + "PBR_Material_Box_Out.usdz");

{{< /highlight >}}

## Relation objets d'animation
Aspose.3D fournit un support d'animation au niveau des données, et le support de calcul est en cours de développement.

Dans Aspose.3D, une scène peut contenir plusieurs objets AnimationClip. Chaque clip d'animation peut être composé de plusieurs nœuds d'animation. Le nœud d'animation suit le modèle de conception composite, ce qui permet la création de structures hiérarchiques avec des nœuds d'animation secondaire.

Les nœuds d'animation peuvent être associés à des points de liaison, qui définissent les propriétés de l'objet cible qui sera animé. Les vecteurs sont des types de données couramment utilisés dans de nombreuses propriétés d'entité. Par conséquent, les points de liaison peuvent avoir différents canaux d'animation pour mettre à jour des canaux spécifiques du vecteur indépendamment. Chaque canal contient une séquence d'images clés qui définit la façon dont la valeur est animée dans le temps.

Ce système fournit un cadre flexible pour animer des objets dans une scène. En définissant des clips d'animation, des nœuds, des points de liaison et des canaux, vous pouvez créer des animations complexes et dynamiques qui affectent diverses propriétés des entités dans votre scène 3D.

Alors que Aspose.3D prend actuellement en charge l'animation au niveau des données, le développement en cours se concentre sur l'extension du support de calcul, ce qui améliorera les capacités de création et de manipulation des animations dans le cadre.

! [Animations](animations.png)


Une scène avec des animations peut avoir ce genre de structure:


! [Animations Échantillon](animation_relations.png)