---
title: Anpassa icke-PBR till PBR material konvertering innan Spara 3D Scener till GLTF 2.0 Format
type: docs
weight: 50
url: /sv/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Scenklass Aspose.3D for Java API representerar en 3D scen och utvecklare kan bygga en 3D scen genom att lägga till olika enheter.
---
{{% alert color="primary" %}} 

Klassen `Scene` Aspose.3D for Java API representerar en 3D scen. och utvecklare kan bygga en 3D scen genom att lägga till olika enheter. GLTF 2.0 stöder endast PBR-material (Fysiskt baserad rendering). Aspose.3D API internt omvandlar icke-PBR-material till PBR-material före export till GLTF 2,0 (materialet i scenen kommer att förbli oförändrat under exporten), och utvecklarna kan ge anpassad konvertera funktion för att åsidosätta standardben Beteende.

{{% /alert %}} 
## **Omvandling av material som inte omfattas av PBR till PBR**
Detta kodexempel visar hur man konverterar material till PBR material, och sedan sparar 3D scen i GLTF format:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Non_PBRtoPBRMaterial.java" >}}
