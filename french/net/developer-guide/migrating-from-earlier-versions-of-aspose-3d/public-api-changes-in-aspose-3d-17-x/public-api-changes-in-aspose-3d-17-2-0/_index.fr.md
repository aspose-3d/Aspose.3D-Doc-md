---
title: Public API Changements dans Aspose.3D 17.2.0
type: docs
weight: 10
url: /fr/net/public-api-changes-in-aspose-3d-17-2-0/
---
**Résumé du contenu**

- [Importation de fichiers DirectX X](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [Ajoute Aspose.ThreeD.Formats.X. Classe XLoadOptions](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.3D API de la version 17.1.0 à 17.2.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses du Aspose.3D.

{{% /alert %}} 
#### **Importation de fichiers DirectX X**
En utilisant la version récente (17.02) ou supérieure, les développeurs peuvent importer des fichiers X. Les entrées au format XBinary et XText sont ajoutées pour importer des fichiers binaires et ASCII X.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
#### **Ajoute Aspose.ThreeD.Formats.X. Classe XLoadOptions**
Nous avons ajouté la classe XLoadOptions. Il aide à importer des fichiers X dans Aspose.3D API.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// initialize Scene class object

Scene scene = new Scene();

// initialize an object

XLoadOptions loadXOpts = new XLoadOptions();

// load X file

scene.Open( "3DX.x", loadXOpts);

{{< /highlight >}}
