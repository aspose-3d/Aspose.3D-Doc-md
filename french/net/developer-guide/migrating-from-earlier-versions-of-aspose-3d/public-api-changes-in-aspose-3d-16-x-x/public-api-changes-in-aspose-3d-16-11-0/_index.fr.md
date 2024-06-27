---
title: Public API Changements dans Aspose.3D 16.11.0
type: docs
weight: 20
url: /fr/net/public-api-changes-in-aspose-3d-16-11-0/
---
**Résumé du contenu**

- [Ajoute la méthode AddEntity dans la classe Aspose.ThreeD.Node](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [Importation et exportation de fichiers glTF](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
-[Ajoute Aspose.ThreeD.Formats.GLTFLoadOptions Classe](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)
-[Ajoute la classe Aspose.ThreeD.Formats.GLTFSaveOptions](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)
-[Ajoute une entrée de format glTF dans la classe Aspose.ThreeD.FileFormat](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)
-[Ajoute une propriété Extension dans la classe Aspose.ThreeD.FileFormatType](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)
- [Ecrire des dépendances dans le système de fichiers réels](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
-[Ajoute la classe Aspose.ThreeD.Utilities.DummyFileSystem](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)
-[Ajoute Aspose.ThreeD.Utilities.LocalFileSystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)
-[Ajoute Aspose.ThreeD.Utilities.MemoryFileSystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)
- [Ajoute la propriété FileSystem dans la classe Aspose.ThreeD.Formats.IOConfig](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

Ce document décrit les modifications apportées à la version Aspose.3D API de la version 16.9.0 à la version 16.11.0, qui peuvent intéresser les développeurs de modules/applications. Il inclut non seulement des méthodes publiques nouvelles et mises à jour, mais aussi une description de tout changement de comportement dans les coulisses de Aspose.3D.

{{% /alert %}} 
###  **Ajoute la méthode AddEntity dans la classe Aspose.ThreeD.Node**
Un moyen de raccourci pour ajouter une entité à un nœud.

**Ajouter une entité à un nœud**

{{< highlight "java" >}}

 // initialize a Scene class object

Scene scene = new Scene();

// create a node

Node sphere = scene.RootNode.CreateChildNode("sphere");

// the old way to add an entity in a node

sphere.Entities.Add(new Sphere());

//the new way to add an entity in a node

sphere.AddEntity(new Sphere());

{{< /highlight >}}
###  **Importation et exportation de fichiers glTF**
En utilisant la version récente (16.11.0) ou supérieure, les développeurs peuvent importer et exporter des fichiers glTF vers/depuis d'autres fichiers 3D pris en charge.
####  **Ajoute Aspose.ThreeD.Formats.GLTFLoadOptions Classe**
Nous avons ajouté la classe GLTFLoadOptions. Il aide à importer des fichiers glTF dans Aspose.3D API.

**Retournez la coordination de la texture V/T**

{{< highlight "java" >}}

 Scene scene = new Scene();

GLTFLoadOptions loadOpt = new GLTFLoadOptions();

//The default value is true, usually we don't need to change it.

//Aspose.3D will automatically flip the V/T texture coordinate during load and save.

//to make sure it's compatible with Aspose.3D

loadOpt.FlipTexCoordV = true;

scene.Open("Duck.gltf", loadOpt);

{{< /highlight >}}
####  **Ajoute la classe Aspose.ThreeD.Formats.GLTFSaveOptions**
Nous avons ajouté la classe GLTFSaveOptions. Il définit les paramètres de sauvegarde d'un fichier glTF.

**Intégrer des dépendances à l'intérieur du fichier de sortie glTF**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and embed all assets into the target file

// usually a glTF file comes with some dependencies, a bin file for model's vertex/indices, two .glsl files for vertex/fragment shaders

// use opt.EmbedAssets to tells the aspose.3D to export scene and embed the dependencies inside the target file.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.EmbedAssets = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Utilisez KHR_materials_Extensions pour définir les matériaux**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and use KHR_materials_common extensions to define the materials

// thus no GLSL files are generated.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.UseCommonMaterials = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Personnaliser le nom du fichier tampon**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and the buffer file that defined the model to customize the filename

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.BufferFile = "mybuf.bin";

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Crée un fichier binaire glTF en utilisant l'extension KHR_binary_glTF**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**Crée un fichier binaire glTF en utilisant l'extension KHR_binary_glTF avec options de sauvegarde**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension but allow you to configure the save options

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// use saving options

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.Binary);

opt.UseCommonMaterials = true;

// save 3D file

scene.Save("d:\\test.glb", opt);

{{< /highlight >}}
####  **Ajoute une entrée de format glTF dans la classe Aspose.ThreeD.FileFormat**
Nous avons ajouté des entrées au format GLTF et GLTF_Binary à des fins de chargement et de sauvegarde.
####  **Ajoute une propriété Extension dans la classe Aspose.ThreeD.FileFormatType**
Nous avons ajouté une propriété Extension dans la classe FileFormatType pour obtenir le nom d'extension du format de fichier.
###  **Ecrire des dépendances dans le système de fichiers réels**
En utilisant la version récente (16.11.0) ou supérieure, les développeurs peuvent enregistrer toutes les dépendances de scène 3D dans le système de fichiers réel. Les développeurs peuvent définir le chemin d'un répertoire local, enregistrer dans l'objet MemoryFileSystem ou simplement jeter les dépendances. La propriété FileSystem est ajoutée dans toutes les classes d'option de sauvegarde.
####  **Ajoute la classe Aspose.ThreeD.Utilities.DummyFileSystem**
**Jeter l'enregistrement des fichiers matériels**

{{< highlight "java" >}}

 // the code example uses the DummyFileSystem, so the material files are not created.

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere()).Material = new PhongMaterial();

// set saving options

ObjSaveOptions opt = new ObjSaveOptions();

opt.FileSystem = new DummyFileSystem();

// save 3D scene

scene.Save("d:\\test.obj", opt);

{{< /highlight >}}
####  **Ajoute Aspose.ThreeD.Utilities.LocalFileSystem Class**
**Sauvegardez les dépendances dans le répertoire local**

{{< highlight "java" >}}

 // the code example uses the LocalFileSystem class to save dependencies to the local directory.

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere()).Material = new PhongMaterial();

// set saving options

ObjSaveOptions opt = new ObjSaveOptions();

opt.FileSystem = new LocalFileSystem("E:\\");

// save 3D scene

scene.Save("d:\\test.obj", opt);

{{< /highlight >}}
####  **Ajoute Aspose.ThreeD.Utilities.MemoryFileSystem Class**
**Sauvegardez les dépendances dans l'objet MemoryFileSystem**

{{< highlight "java" >}}

 // the code example uses the MemoryFileSystem to intercepts the dependencies writing.

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere()).Material = new PhongMaterial();

// set saving options

ObjSaveOptions opt = new ObjSaveOptions();

MemoryFileSystem mfs = new MemoryFileSystem();

opt.FileSystem = mfs;

// save 3D scene

scene.Save("d:\\test.obj", opt);

//get the test.mtl file content

byte[] mtl = mfs.GetFileContent("test.mtl");

File.WriteAllBytes("material.mtl", mtl);

{{< /highlight >}}
###  **Ajoute la propriété FileSystem dans la classe Aspose.ThreeD.Formats.IOConfig**
Nous avons ajouté une propriété FileSystem dans la classe IOConfig pour écrire des dépendances.

**Ajoute une propriété FileSystem**

{{< highlight "java" >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
