---
title: Public API Changements dans Aspose.3D 16.9.0
type: docs
weight: 30
url: /fr/net/public-api-changes-in-aspose-3d-16-9-0/
---
**Résumé du contenu**

- [Importer 3D Scène de la Source PDF](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
  - [Ajoute Aspose.ThreeD.Formats. Classe PdfLoadOptions](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)
  - [Ajoute Aspose.ThreeD.FileFormat et Aspose.ThreeD.Formats. Classe PdfFormat](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)
- [Économisez une scène 3D au format PDF](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
  - [Ajoute Aspose.ThreeD.Formats. Classe PdfSaveOptions et Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode Enums](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)
- [Ajoute la méthode triangulée dans le Aspose.ThreeD. Entités. Classe de polygonmodificateur](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Ajoute deux méthodes BuildTangentBinormal dans le Aspose.ThreeD. Entités. Classe de polygonmodificateur](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.3D API de la version 2.1.0 à 16.9.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses du Aspose.3D.

{{% /alert %}} 
### **Importer 3D Scène de la Source PDF**
En utilisant la version récente (16.9.0) ou supérieure, les développeurs peuvent récupérer des scènes 3D à partir d'un fichier d'entrée PDF.
#### **Ajoute Aspose.ThreeD.Formats. Classe PdfLoadOptions**
Nous avons ajouté la classe PdfLoadOptions. Il aide à charger le contenu à partir du fichier d'entrée PDF. Les développeurs peuvent appliquer un mot de passe pour les PDF protégés.

**Scène ouverte à partir d'un fichier PDF protégé par mot de passe**

{{< highlight "java" >}}

 // set path with filename and extension 

string path = @"House_Design.pdf";

// create a new scene

Scene scene = new Scene();

// use loading options and apply password

PdfLoadOptions opt = new PdfLoadOptions() {Password = Encoding.UTF8.GetBytes("password")};

// open scene

scene.Open(path, opt);

{{< /highlight >}}
#### **Ajoute Aspose.ThreeD.FileFormat et Aspose.ThreeD.Formats. Classe PdfFormat**
Nous avons ajouté une entrée au format PDF dans la classe FileFormat à des fins de chargement et d'économie. La classe PdfFormat aide à manipuler les PDF.

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**Extraire tout le contenu brut 3D du fichier PDF**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[]password = null;

// extract 3D contents

List<byte[]> contents = FileFormat.PDF.Extract(path, password);

int i = 1;

// iterate through the contents and in separate 3D files

foreach (byte[]content in contents)

{

    string fileName = "3d-" + (i++);

    File.WriteAllBytes(fileName, content);

}

{{< /highlight >}}

**Extrayez toutes les scènes 3D et enregistrez-les dans le fichier FBX**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[]password = null;

List<Scene> scenes = FileFormat.PDF.ExtractScene(path, password);

int i = 1;

// iterate through the scenes and save in 3D files

foreach (Scene scene in scenes)

{

    string fileName = "3d-" + (i++) + ".fbx";

    scene.Save(fileName, FileFormat.FBX7400ASCII);

}

{{< /highlight >}}
### **Économisez une scène 3D au format PDF**
En utilisant la version récente (16.9.0) ou supérieure, les développeurs peuvent enregistrer tous les fichiers 3D pris en charge au format PDF.
#### **Ajoute Aspose.ThreeD.Formats. Classe PdfSaveOptions et Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode Enums**
Le PdfSaveOptions aide à appliquer le réglage avant l'enregistrement au format de sortie PDF. Les développeurs peuvent définir un mode de rendu et un schéma d'éclairage avant d'enregistrer une scène 3D au format PDF comme ci-dessous:

**Créer un 3D PDF avec un cylindre, et rendu en mode illustration ombrée avec un éclairage optimisé CAD**

{{< highlight "java" >}}

 // create a new scene

Scene scene = new Scene();

// create a cylinder child node

scene.RootNode.CreateChildNode("cylinder", new Cylinder()).Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.DarkCyan)};

// set rendering mode and lighting scheme

PdfSaveOptions opt = new PdfSaveOptions();

opt.LightingScheme = PdfLightingScheme.CAD;

opt.RenderMode = PdfRenderMode.ShadedIllustration;

// save in the PDF format

scene.Save("output.pdf", opt);

{{< /highlight >}}
### **Ajoute la méthode triangulée dans le Aspose.ThreeD. Entités. Classe de polygonmodificateur**
Nous avons ajouté une autre surcharge de la méthode Triangulate dans la classe PolygonModifier qui prend un objet de classe Scène comme paramètre.

**Convertir tous les polygones en triangles dans le fichier FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
### **Ajoute deux méthodes BuildTangentBinormal dans le Aspose.ThreeD. Entités. Classe de polygonmodificateur**
Nous avons ajouté deux méthodes BuildTangentBinormal dans la classe PolygonModifier. Une méthode prend l'objet de classe Scène comme paramètre et une autre prend l'objet de classe Mesh comme paramètre.

**Construire des données tangentes et binormales pour tous les mailles dans le fichier FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
