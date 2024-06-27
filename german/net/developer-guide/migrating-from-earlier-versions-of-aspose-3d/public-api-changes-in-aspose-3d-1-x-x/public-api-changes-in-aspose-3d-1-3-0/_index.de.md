---
title: Öffentliche API Änderungen in Aspose.3D 1.3.0
type: docs
weight: 40
url: /de/net/public-api-changes-in-aspose-3d-1-3-0/
---
**Inhalts übersicht**

- [Names pace und Klassen namen ändern sich](#PublicAPIChangesinAspose.3D1.3.0-Namespaceandclassnamechanges)
- [Erstellen Sie einen Scheitel punkt, indem Sie die Referenz-und Kartierung smodi zuweisen](#PublicAPIChangesinAspose.3D1.3.0-CreateVertexbyAssigningtheReferenceandMappingModes)
- [Universal 3D Die Spar option wird im File Format hinzugefügt](#PublicAPIChangesinAspose.3D1.3.0-Universal3DSavingOptionisaddedintheFileFormat)
- [Rohe Inhalte in die Textur von FBX einbetten](#PublicAPIChangesinAspose.3D1.3.0-EmbedRawContenttotheTextureofFBX)
- [Die Zersetzen-Methode wird in der Matrix4-Klasse hinzugefügt](#PublicAPIChangesinAspose.3D1.3.0-DecomposemethodisaddedintheMatrix4class)
- [Ein neuer Konstruktor in der Vector4-Klasse wird hinzugefügt, um einen Vector3-Objektparameter zu erhalten](#PublicAPIChangesinAspose.3D1.3.0-AnewconstructorinVector4classisaddedtoreceiveaVector3objectparameter)

{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.3D API von Version 1.2.0 bis 1.3.0, die für Modul-/Anwendungs entwickler von Interesse sein können. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.3D.

{{% /alert %}} 
###  **Names pace und Klassen namen ändern sich**
- Names pace Aspose.ThreeD. Animationen geändert zu Aspose.ThreeD.Animation
- Klasse Aspose.ThreeD. Animationen. Animation geändert in Aspose.ThreeD.Animation.Animation Node
- Names pace Aspose.ThreeD.IO in Aspose geändert. ThreeD. Formate
- Names pace Aspose.ThreeD.Utils in Aspose geändert. ThreeD.Utilities
###  **Erstellen Sie einen Scheitel punkt, indem Sie die Referenz-und Kartierung smodi zuweisen**
Entwickler können einen Scheitel punkt erstellen, indem sie den Referenz-und Mapping-Modus in einer einzigen Code zeile zuweisen. Beispiel code:

{{% alert color="primary" %}} 

Das Mesh-Klassen objekt wird im Code verwendet. Wir können [Erstellen Sie ein Mesh-Klassen objekt, wie es dort erzählt wird](/pages/createpage.action?spaceKey=3dnet&title=Create+a+3D+Cube+Mesh&linkCreation=true&fromPageId=19923253).

{{% /alert %}} 

**C#**

{{< highlight "csharp" >}}

 // call overloaded CreateElement method of the Mesh object

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;

{{< /highlight >}}

###  **Universal 3D Die Spar option wird im File Format hinzugefügt**
Die Option Universal 3D Format wurde in der FileFormat-Enumer hinzugefügt. Beispiel code:

**C#**

{{< highlight "csharp" >}}

 // save scene in the Universal3D format

scene.Save("C:\\temp\\Output.fbx", FileFormat.Universal3D);

{{< /highlight >}}

###  **Rohe Inhalte in die Textur von FBX einbetten**
Die<tt>Inhalt</tt>Eigenschaft hat hinzugefügt<tt>Textur</tt>Klasse, um den Roh inhalt in die Textur des FBX-Dokuments einzubetten. Beispiel code:

**C#**

{{< highlight "csharp" >}}

 // initialize Texture class object

Texture texture = new Texture();

// set file name

texture.FileName = "embedded-texture.png";

// set binary content

texture.Content = File.ReadAllBytes("c:\\test.png");

{{< /highlight >}}

###  **Die Zersetzen-Methode wird in der Matrix4-Klasse hinzugefügt**
Es ist eine mathematische Nutzen funktion, die verwendet wird, um eine affine Transformation matrix zu zerlegen.
###  **Ein neuer Konstruktor in der Vector4-Klasse wird hinzugefügt, um einen Vector3-Objektparameter zu erhalten**
Es erleichtert die Konstruktion eines Vector4 auf Basis des Vector3. Der vierte Wert des Vector4 zeigt die Ebene w und sein Standardwert ist 1.
