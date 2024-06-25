---
title: Passen Sie die Konvertierung von Nicht-PBR-Materialien an, bevor Sie 3D-Szenen in GLTF 2,0-Format in C# speichern
linktitle: Passen Sie die Konvertierung von Nicht-PBR-Materialien an, bevor Sie 3D-Szenen in das GLTF 2,0-Format speichern
type: docs
weight: 70
url: /de/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Die Scene-Klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können bereits eine 3D-Szene erstellen, indem sie verschiedene Entitäten hinzufügen. GLTF 2.0 unterstützt nur PBR-Materialien (Physically Based Rendering), Aspose.3D API wandelt nicht-PBR-Materialien intern in PBR-Materialien um, bevor sie in GLTF 2,0 exportiert werden.
---
{{% alert color="primary" %}} 

Die [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können bereits eine 3D-Szene erstellen, indem sie verschiedene Entitäten hinzufügen. GLTF 2.0 unterstützt nur PBR-Materialien (Physically Based Rendering), Aspose.3D API wandelt Nicht-PBR-Materialien intern in PBR-Materialien um, bevor sie in GLTF 2.0 exportiert werden (die Materialien in der Szene bleiben während des Exports unverändert), und die Entwickler können eine benutzer definierte Konvertierungs funktion bereitstellen, um das Standard verhalten außer Kraft zu setzen.

{{% /alert %}} 
##  **Nicht-PBR-zu-PBR-Material umwandlung**
Dieses C#-Code beispiel zeigt, wie Sie Material in PBR-Material konvertieren und dann eine 3D-Szene im GLTF-Format mit einer C# 3D-Datei manipulation und-konvertierung API speichern:

**C#**

{{< highlight "java" >}}

 // initialize a new 3D scene

var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = (Material material) => {
    var pbr = PbrMaterial.FromMaterial(material);
    //customize your own PBR material here, you can get the original OBJ's material from the parameter mat.
    //to create a compatible material with obj2gltf, use following definition:
    pbr.MetallicFactor = 0;
    pbr.RoughnessFactor = 0.98;
    return pbr;
};

// save in GLTF 2.0 format

s.Save("test.gltf", opt);

{{< /highlight >}}


##  **Ressourcen**

1. [Online-Tutorial](https://products.aspose.com/3d/tutorial/use-phong-material-to-pbr-material/)
