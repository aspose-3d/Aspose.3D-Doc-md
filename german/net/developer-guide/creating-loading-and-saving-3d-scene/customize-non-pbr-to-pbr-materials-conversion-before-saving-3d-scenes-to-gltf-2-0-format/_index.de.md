---
title: Passen Sie die Umwandlung von Nicht-PBR-Materialien an, bevor Sie 3D Szenen in GLTF 2.0-Format in C# speichern
linktitle: Passen Sie die Umwandlung von Nicht-PBR-Materialien an, bevor Sie die Szenen 3D in das Format GLTF 2.0 speichern
type: docs
weight: 70
url: /de/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Die Szene klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können bereits eine 3D-Szene erstellen, indem sie verschiedene Entitäten hinzufügen. GLTF 2.0 unterstützt nur PBR-Materialien (Physically Based Rendering), Aspose.3D API wandelt Nicht-PBR-Materialien intern in PBR-Materialien um, bevor es in GLTF 2.0 exportiert.
---
{{% alert color="primary" %}} 

Die [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können bereits eine 3D-Szene erstellen, indem sie verschiedene Entitäten hinzufügen. GLTF 2.0 unterstützt nur PBR-Materialien (Physically Based Rendering), Aspose.3D API wandelt Nicht-PBR-Materialien intern in PBR-Materialien um, bevor sie in GLTF 2.0 exportiert (die Materialien in der Szene bleiben während des Exports unverändert), und die Entwickler können benutzer definierte Konvertierungs funktion bereitstellen das Standard verhalten außer Kraft setzen.

{{% /alert %}} 
## **Nicht-PBR-zu-PBR-Material umwandlung**
Dieses Code beispiel C# zeigt, wie Material in PBR-Material umgewandelt wird, und speichert dann die 3D-Szene im Format GLTF mit der Manipulation und Konvertierung der API-Datei API:

**C#**

{{< highlight "java" >}}

 // initialize a new 3D scene

var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = delegate(Material material)

{

    PhongMaterial m = (PhongMaterial) material;

    return new PbrMaterial() {Albedo = new Vector3(m.DiffuseColor.x, m.DiffuseColor.y, m.DiffuseColor.z)};

};

// save in GLTF 2.0 format

s.Save("test.gltf", opt);

{{< /highlight >}}
