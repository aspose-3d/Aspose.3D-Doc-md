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

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
/* initialize a new 3D scene */
Scene s = new Scene();
Box box = new Box();
PhongMaterial mat = new PhongMaterial();
mat.setDiffuseColor(new Vector3(1, 0, 1));
s.getRootNode().createChildNode("box1", box).setMaterial(mat);
GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);
//Custom material converter to convert PhongMaterial to PbrMaterial
opt.setMaterialConverter(new MaterialConverter() {
    @Override
    public Material call(Material material) {
        PhongMaterial m = (PhongMaterial) material;
        PbrMaterial ret = new PbrMaterial();
        ret.setAlbedo(m.getDiffuseColor());
        return ret;
    }
});
// save in GLTF 2.0 format
s.save(MyDir + "Non_PBRtoPBRMaterial_Out.gltf", opt);
{{< /highlight >}}
