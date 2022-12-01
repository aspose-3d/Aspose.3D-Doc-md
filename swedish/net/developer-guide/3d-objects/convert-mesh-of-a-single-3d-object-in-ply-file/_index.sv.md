---
title: Konvertera Mesh för ett enda 3D objekt i PLY
type: docs
weight: 20
url: /sv/net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Den överbelastade EncodeMesh medlemmar som exponeras av PlyFormat klassen kan användas för att konvertera mesh av en 3D objekt. till PLY. EncodeMesh medlemmar tar Mesh, utdatafilnamn och PlySaveOptions objekt som parametrar. Med hjälp av PLY sparalternativ kan utvecklare ändra namnet på koordinatkomponenter.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API tillåter utvecklare att konvertera Mesh av en enda 3D objekt i filen PLY.

{{% /alert %}}
## **Skapa ett 3D objekt och spara det till PLY-fil.**
De överbelastade `EncodeMesh` medlemmar som exponeras av klassen `PlyFormat` kan användas för att konvertera `Mesh` av en `Mesh` 3D objekt till PLY-fil. De `EncodeMesh` medlemmar tar `Mesh`, utdata filnamn och `PlySaveOptions` objekt som parametrar. Med hjälp av PLY sparalternativ kan utvecklare ändra namnet på koordinatkomponenter.
### **Programmeringsprova**
Detta kodexempel skapar ett 3D Cylinderobjekt, och sedan koda i filen PLY.

**C#**

{{< highlight "java" >}}

 // Create a cylinder object and save it to ply file

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply");

/* using Ply save options*/

//Save as binary PLY format, the default value is ASCII

PlySaveOptions opt = new PlySaveOptions(FileContentType.Binary);

//change the components to 's' and 't'

opt.TextureCoordinateComponents.Item1 = "s";

opt.TextureCoordinateComponents.Item2 = "t";

//save the mesh

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply", opt);

{{< /highlight >}}
