---
title: Public API Changements dans Aspose.3D 16.12.0
type: docs
weight: 10
url: /fr/net/public-api-changes-in-aspose-3d-16-12-0/
---
**Résumé du contenu**

- [Ajoute Aspose.ThreeD. Classe mesurée](#PublicAPIChangesinAspose.3D16.12.0-AddsAspose.ThreeD.MeteredClass)
- [Importation de fichiers DXF](#PublicAPIChangesinAspose.3D16.12.0-ImportingDXFFiles)

{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.3D API de la version 16.11.0 à 16.12.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses du Aspose.3D.

{{% /alert %}} 
### **Ajoute Aspose.ThreeD. Classe mesurée**
Un moyen d'appliquer une licence au compcompère.

**C#**

{{< highlight "java" >}}

 // initialize a metered license class object

Metered metered = new Metered();

// set public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

//Your other code to use Aspose.3D

{{< /highlight >}}
### **Importation de fichiers DXF**
En utilisant la version récente (16.12.0) ou plus, les développeurs peuvent importer des fichiers DXF. L'entrée de format DXF est ajoutée à des fins de chargement.

**C#**

{{< highlight "java" >}}

 // an entry of DXF file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat DXF;

// load a DXF file

Scene dxfFile = new Scene("wuson.dxf");

{{< /highlight >}}
