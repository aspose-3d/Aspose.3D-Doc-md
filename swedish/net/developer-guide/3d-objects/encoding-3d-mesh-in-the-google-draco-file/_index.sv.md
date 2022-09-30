---
title: Kodning 3D Mesh i Google Draco Arkiv
type: docs
weight: 60
url: /sv/net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for .NET API ger utvecklare möjlighet att importera en 3D modell, och sedan koda maskor i filerna Google Draco. Utvecklare kan också ange position, struktur koordinater, färg och normala bitar samt komprimeringsnivå innan kodning av en mesh.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API tillåter utvecklare att[Importera en 3D modell](/3d/sv/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), Och sedan koda maskor i filerna Google Draco. Utvecklare kan också ange position, struktur koordinater, färg och normala bitar samt komprimeringsnivå innan kodning av en mesh.

{{% /alert %}}
## **Hämta en 3D Mesh och koda i Google Draco Arkiv**
Den `Encode`-metod som exponeras i klassen [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) kan användas för att koda en 3D-mask i Google Draco filen. Det tar en [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) och [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) objekt som parametrar. Med hjälp av Draco sparalternativ kan utvecklare också ange position, texturkoordinater, färg och normala bitar samt kompressionsnivå före kodning av en mesh.
### **Programmeringsprova**
Detta kodexempel hämtar en `Mesh` av `Sphere`, och sedan koda i filen Google Draco efter angiven komprimeringsnivå.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.cs" >}}
