---
title: Kodning 3D Mesh i Google Draco Arkiv
type: docs
weight: 60
url: /sv/python-net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D för Python via .NET API ger utvecklare möjlighet att importera en 3D modell, och sedan koda maskor i filerna Google Draco. Utvecklare kan också ange position, struktur koordinater, färg och normala bitar samt komprimeringsnivå innan kodning av en mesh.
---
{{% alert color="primary" %}}

[Aspose.3D för Python via .NET](https://products.aspose.com/3d/python-net/)API tillåter utvecklare att[Importera en 3D modell](/3d/sv/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), Och sedan koda maskor i filerna Google Draco. Utvecklare kan också ange position, struktur koordinater, färg och normala bitar samt komprimeringsnivå innan kodning av en mesh.

{{% /alert %}}
## **Hämta en 3D Mesh och koda i Google Draco Arkiv**
Den `encode`-metod som exponeras i klassen [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) kan användas för att koda en 3D-mask i Google Draco filen. Det tar en [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) och [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) objekt som parametrar. Med hjälp av Draco sparalternativ kan utvecklare också ange position, texturkoordinater, färg och normala bitar samt kompressionsnivå före kodning av en mesh.
### **Programmeringsprova**
Detta kodexempel hämtar en Mesh of Sphere, och sedan koda i filen Google Draco efter angiven komprimeringsnivå.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.py" >}}
