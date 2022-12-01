---
title: Public API Changements dans Aspose.3D 1.1.0
type: docs
weight: 60
url: /fr/net/public-api-changes-in-aspose-3d-1-1-0/
---
**Résumé du contenu**

- [L'option d'économie FBX7200ASCII est ajoutée dans le FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [L'option d'économie binaire FBX7200est ajoutée au format FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [L'option d'économie FBX7300ASCII est ajoutée dans le FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [L'option d'économie binaire FBX7300est ajoutée au format FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [L'option d'économie WavefrontOBJ est ajoutée dans FileFormat et FileFormatType](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.3D API de la version 1.0.0 à 1.1.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses du Aspose.3D.

{{% /alert %}} 
### **L'option d'économie FBX7200ASCII est ajoutée dans le FileFormat**
L'option de format FBX7200ASCII a été ajoutée dans l'enum FileFormat. Il représente le format de fichier ASCII FBX, avec la version 7.2.0. Exemple de code:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

### **L'option d'économie binaire FBX7200est ajoutée au format FileFormat**
L'option de format FBX7200Binary a été ajoutée dans l'enum FileFormat. Il représente le format de fichier Binary FBX, avec la version 7.2.0. Exemple de code:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

### **L'option d'économie FBX7300ASCII est ajoutée dans le FileFormat**
L'option de format FBX7300ASCII a été ajoutée dans l'enum FileFormat. Il représente le format de fichier ASCII FBX, avec la version 7.3.0. Exemple de code:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

### **L'option d'économie binaire FBX7300est ajoutée au format FileFormat**
L'option de format binaire FBX7300a été ajoutée dans l'enum FileFormat. Il représente le format de fichier Binary FBX, avec la version 7.3.0. Exemple de code:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

### **L'option d'économie WavefrontOBJ est ajoutée dans FileFormat et FileFormatType**
L'option de format WavefrontOBJ a été ajoutée dans les énums FileFormat et FileFormatType. Il représente le format de fichier Obj de Wavefront. Exemple de code:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

