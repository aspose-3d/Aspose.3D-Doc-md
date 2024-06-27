---
title: Konvertera ett enda objekt i 3D fil i PLY
type: docs
weight: 20
url: /sv/net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: De överbelastade EncodeMesh-medlemmarna som exponeras av PlyFormat-klassen kan användas för att konvertera mesh för ett 3D-objekt till PLY fil. EncodeMesh medlemmar tar Mesh, utdatafilnamn och PlySaveOptions objekt som parametrar. Med PLY sparningsalternativ kan utvecklare ändra namnet på koordinatkomponenter.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API tillåter utvecklare att konvertera mesh för ett enda 3D objekt i filen PLY.

{{% /alert %}}
##  **Skapa ett 3D-objekt och spara det i PLY-filen**
De överbelastade `EncodeMesh` medlemmar som exponeras av klassen `PlyFormat` kan användas för att konvertera `Mesh` i ett 3D objekt till PLY fil. `EncodeMesh` medlemmarna tar `Mesh`, utfilnamnet och `PlySaveOptions` objekt som parametrar. Med PLY sparningsalternativ kan utvecklare ändra namnet på koordinatkomponenter.
###  **Programmeringsprova**
Det här kodexemplet skapar ett 3D Cylinderobjekt och kodar sedan i filen PLY.

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
