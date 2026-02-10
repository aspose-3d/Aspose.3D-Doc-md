---
title: Personnaliser la conversion des matériaux non-PBR en PBR avant de sauvegarder les scènes 3D au format GLTF 2.0
type: docs
weight: 50
url: /fr/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La classe Scene de la Aspose.3D for Java API représente une scène 3D et les développeurs peuvent construire une scène 3D en ajoutant diverses entités.
---
{{% alert color="primary" %}} 

La classe `Scene` de la Aspose.3D for Java API représente une scène 3D et les développeurs peuvent construire une scène 3D en ajoutant diverses entités. GLTF 2.0 prend uniquement en charge les matériaux PBR (Physically Based Rendering), Aspose.3D API convertit en interne les matériaux non-PBR en matériaux PBR avant d'exporter en GLTF 2.0 (les matériaux de la scène resteront inchangés pendant l'exportation), et les développeurs peuvent fournir une fonction de conversion personnalisée pour remplacer le comportement par défaut.

{{% /alert %}} 
##  **Conversion de matériaux non-PBR vers PBR**
Cet exemple de code montre comment convertir du matériau en matériau PBR, puis enregistre la scène 3D au format GLTF:

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
