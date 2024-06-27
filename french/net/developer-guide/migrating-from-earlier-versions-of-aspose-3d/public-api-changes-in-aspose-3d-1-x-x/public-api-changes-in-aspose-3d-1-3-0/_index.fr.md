---
title: Public API Changements dans Aspose.3D 1.3.0
type: docs
weight: 40
url: /fr/net/public-api-changes-in-aspose-3d-1-3-0/
---
**Résumé du contenu**

- [Changements d'espace de noms et de nom de classe](#PublicAPIChangesinAspose.3D1.3.0-Namespaceandclassnamechanges)
- [Créer un sommet en attribuant les modes de référence et de cartographie](#PublicAPIChangesinAspose.3D1.3.0-CreateVertexbyAssigningtheReferenceandMappingModes)
- [Universal 3D Saving Option est ajouté dans le FileFormat](#PublicAPIChangesinAspose.3D1.3.0-Universal3DSavingOptionisaddedintheFileFormat)
- [Incorporer du contenu brut à la texture de FBX](#PublicAPIChangesinAspose.3D1.3.0-EmbedRawContenttotheTextureofFBX)
- [La méthode de décomposition est ajoutée dans la classe Matrix4](#PublicAPIChangesinAspose.3D1.3.0-DecomposemethodisaddedintheMatrix4class)
- [Un nouveau constructeur dans la classe Vector4 est ajouté pour recevoir un paramètre d'objet Vector3](#PublicAPIChangesinAspose.3D1.3.0-AnewconstructorinVector4classisaddedtoreceiveaVector3objectparameter)

{{% alert color="primary" %}} 

Ce document décrit les changements apportés à Aspose.3D API de la version 1.2.0 à 1.3.0, qui peuvent intéresser les développeurs de modules/applications. Il inclut non seulement des méthodes publiques nouvelles et mises à jour, mais aussi une description de tout changement de comportement dans les coulisses de Aspose.3D.

{{% /alert %}} 
###  **Changements d'espace de noms et de nom de classe**
- Namespace Aspose.ThreeD.Animations changé en Aspose.ThreeD.Animation
- Classe Aspose.ThreeD.Animations.Animation changée en Aspose.ThreeD.Animation.AnimationNode
- Namespace Aspose.ThreeD.IO changé en Aspose.ThreeD.Formats
- Namespace Aspose.ThreeD.Utils changé en Aspose.ThreeD.Utilities
###  **Créer un sommet en attribuant les modes de référence et de cartographie**
Les développeurs peuvent créer un sommet en attribuant les modes Référence et Cartographie dans une seule ligne de code. Exemple de code:

{{% alert color="primary" %}} 

L'objet de classe Mesh est utilisé dans le code. Nous pouvons [Créer un objet de classe Mesh tel que raconté là-bas](/pages/createpage.action?spaceKey=3dnet&title=Create+a+3D+Cube+Mesh&linkCreation=true&fromPageId=19923253).

{{% /alert %}} 

**C#**

{{< highlight "csharp" >}}

 // call overloaded CreateElement method of the Mesh object

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;

{{< /highlight >}}

###  **Universal 3D Saving Option est ajouté dans le FileFormat**
L'option de format Universal 3D a été ajoutée dans l'enum FileFormat. Exemple de code:

**C#**

{{< highlight "csharp" >}}

 // save scene in the Universal3D format

scene.Save("C:\\temp\\Output.fbx", FileFormat.Universal3D);

{{< /highlight >}}

###  **Incorporer du contenu brut à la texture de FBX**
Le<tt>Contenu</tt>La propriété a ajouté au<tt>Texture</tt>Pour intégrer le contenu brut dans la texture du document FBX. Exemple de code:

**C#**

{{< highlight "csharp" >}}

 // initialize Texture class object

Texture texture = new Texture();

// set file name

texture.FileName = "embedded-texture.png";

// set binary content

texture.Content = File.ReadAllBytes("c:\\test.png");

{{< /highlight >}}

###  **La méthode de décomposition est ajoutée dans la classe Matrix4**
C'est une fonction d'utilité mathématique utilisée pour décomposer une matrice de transformation affine.
###  **Un nouveau constructeur dans la classe Vector4 est ajouté pour recevoir un paramètre d'objet Vector3**
Il facilite la construction d'un Vector4 basé sur le Vector3. La quatrième valeur du Vector4 présente le plan w et sa valeur par défaut est 1.
