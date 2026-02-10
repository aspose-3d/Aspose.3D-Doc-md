---
title: Kodning 3D Mesh i Google Draco filen
type: docs
weight: 30
url: /sv/java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose. 3D for Java API har stöd för att importera 3D-modellen, hämta mesh, och kodar sedan mesh i filen Google Draco.
---
{{% alert color="primary" %}} 

Aspose. 3D for Java API har stöd för att importera 3D-modellen, hämta mesh, och kodar sedan mesh i filen Google Draco. Utvecklare kan också ange position, struktur koordinater, färg och normala bitar samt komprimeringsnivå innan kodning av en mesh.

{{% /alert %}} 
##  **Hämta 3D Mesh och koda i Google Draco fil**
Kodmetoden som exponeras av klassen `DracoFormat` kan användas för att koda en 3D-mash i filen Google Draco. Det tar ett `Mesh` och `DracoSaveOptions` objekt som parametrar. Med Draco sparningsalternativ kan utvecklare också ange position, strukturkoordinater, färg och normala bitar samt kompressionsnivå före kodning av en mesh.
###  **Programmeringsprova**
Detta kodexempel hämtar Mesh of Sphere, och koda sedan i filen Google Draco efter att en komprimeringsnivå har angetts.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Create a sphere
Sphere sphere = new Sphere();
// Encode the sphere to Google Draco raw data using optimal compression level.
DracoSaveOptions opt = new DracoSaveOptions();
opt.setCompressionLevel(DracoCompressionLevel.OPTIMAL);
byte[] b = FileFormat.DRACO.encode(sphere.toMesh(), opt);
// Save the raw bytes to file
Files.write(Paths.get(MyDir, "SphereMeshtoDRC_Out.drc"), b);
{{< /highlight >}}
