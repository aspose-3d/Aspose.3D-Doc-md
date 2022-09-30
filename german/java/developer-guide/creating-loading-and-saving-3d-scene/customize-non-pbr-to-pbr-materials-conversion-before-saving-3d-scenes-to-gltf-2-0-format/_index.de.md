---
title: Passen Sie die Umwandlung von Nicht-PBR-Materialien an, bevor Sie die Szenen 3D in das Format GLTF 2.0 speichern
type: docs
weight: 50
url: /de/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Die Scene-Klasse der Aspose.3D for Java API repräsentiert eine 3D-Szene, und Entwickler können eine 3D-Szene erstellen, indem sie verschiedene Entitäten hinzufügen.
---
{{% alert color="primary" %}} 

Die `Scene`-Klasse der Aspose.3D for Java API repräsentiert eine 3D-Szene, und Entwickler können eine 3D-Szene erstellen, indem sie verschiedene Entitäten hinzufügen. GLTF 2.0 unterstützt nur PBR-Materialien (Physically Based Rendering), Aspose.3D API wandelt Nicht-PBR-Materialien intern in PBR-Materialien um, bevor sie in GLTF 2.0 exportiert (die Materialien in der Szene bleiben während des Exports unverändert), und die Entwickler können benutzer definierte Konvertierungs funktion bereitstellen das Standard verhalten außer Kraft setzen.

{{% /alert %}} 
## **Nicht-PBR-zu-PBR-Material umwandlung**
Dieses Code beispiel zeigt, wie Material in PBR-Material umgewandelt wird, und speichert dann die 3D-Szene im Format GLTF:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Non_PBRtoPBRMaterial.java" >}}
