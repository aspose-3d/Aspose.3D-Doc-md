---
title: Exportera texturfiler vid sparning av 3D- scene
type: docs
weight: 10
url: /sv/net/export-texture-files-while-saving-3d-scene
description: Med Aspose.3D for .NET kan utvecklare exportera texturfiler till filsystemet medan 3D scen sparas.
---
{{% alert color="primary" %}}

Använda [Aspose.3D for .NET](https://products.aspose.com/3d/net/) När en scen exporteras till filer är det ofta nödvändigt att exportera texturer. om den är inbäddad eller extern, till samma katalog. Aspose. 3D for .NET underlättar denna process, så att alla texturer hanteras och lagras korrekt tillsammans med den exporterade scenen. Denna guide visar hur man kan uppnå detta.

{{% /alert %}}

För att exportera en scen och se till att alla tillhörande texturer sparas i samma katalog, följ dessa steg:


{{% highlight "csharp" %}}

Scene scene = Scene.FromFile(@"BoomBox.glb");
var opt = new ObjSaveOptions();
opt.ExportTextures = true;
scene.Save(@"D:\tmp\boombox\output.obj", opt);

{{% /highlight %}}


Alla `SaveOptions`-objekt i Aspose.3D inkluderar egenskapen `ExportTextures`, vilket förenklar processen för hantering av texturer under export. Den här egenskapen säkerställer att alla texturer, oavsett om de är externa eller inbäddade, sparas i den angivna utmatningskatalogen. Den här funktionen är kompatibel med olika filformat som stöder texturexport, såsom FBX, 3DS, OBJ, USD, GLTF, och DAE.



Förklaring

1. Ladda scenen: Scenen är laddad från inmatningsfilen.
1. Anpassa sparningsalternativ: Ange `ExportTextures` till `true`.
1. Exportera scenen: Scenen sparas i utmatningskatalogen med de uppdaterade textursökvägarna.


Genom att utnyttja egenskapen `ExportTextures` i `SaveOptions` kan du smidigt exportera 3D scener tillsammans med deras texturer, Se till att alla nödvändiga tillgångar organiseras i en enda katalog. Denna funktion förbättrar bärbarheten och enkel användning av 3D filer över olika plattformar och program.

##  **Resurser**

1. [Online Tutorial](https://products.aspose.com/3d/tutorial/)
1. [SaveOptions](https://reference.aspose.com/3d/net/aspose.threed.formats/saveoptions/)
