---
title: Passen Sie die Konvertierung von Nicht-PBR-Materialien an, bevor Sie 3D-Szenen in das GLTF 2,0-Format speichern
type: docs
weight: 50
url: /de/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Die Scene-Klasse der Aspose.3D for Java API stellt eine 3D-Szene dar, und Entwickler können eine 3D-Szene erstellen, indem sie verschiedene Entitäten hinzufügen.
---
{{% alert color="primary" %}} 

Die `Scene`-Klasse der Aspose.3D for Java API repräsentiert eine 3D-Szene, und Entwickler können eine 3D-Szene erstellen, indem sie verschiedene Entitäten hinzufügen. GLTF 2.0 unterstützt nur PBR-Materialien (Physically Based Rendering), Aspose.3D API konvertiert intern Nicht-PBR-Materialien in PBR-Materialien, bevor sie in GLTF 2.0 exportiert werden (die Materialien in der Szene bleiben während des Exports unverändert), und die Entwickler können eine benutzer definierte Konvertierungs funktion bereitstellen, um das Standard verhalten außer Kraft zu setzen.

{{% /alert %}} 
##  **Nicht-PBR-zu-PBR-Material umwandlung**
Dieses Code beispiel zeigt, wie Material in PBR-Material konvertiert wird, und speichert dann die 3D-Szene im GLTF-Format:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Non_PBRtoPBRMaterial.java" >}}
