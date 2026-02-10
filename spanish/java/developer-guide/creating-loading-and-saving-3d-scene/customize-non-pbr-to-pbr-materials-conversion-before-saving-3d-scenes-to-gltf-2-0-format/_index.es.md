---
title: Personalizar la conversión de materiales no PBR a PBR antes de guardar escenas 3D en formato GLTF 2,0
type: docs
weight: 50
url: /es/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La clase Scene de Aspose.3D for Java API representa una escena 3D y los desarrolladores pueden construir una escena 3D agregando varias entidades.
---
{{% alert color="primary" %}} 

La clase `Scene` de Aspose.3D for Java API representa una escena 3D y los desarrolladores pueden construir una escena 3D agregando varias entidades. GLTF 2,0 solo admite materiales PBR (Physically Based Rendering), Aspose.3D API convierte internamente materiales que no son PBR en materiales PBR antes de exportar a GLTF 2,0 (los materiales en la escena permanecerán sin cambios durante la exportación), y los desarrolladores pueden proporcionar una función de conversión personalizada para anular el comportamiento predeterminado.

{{% /alert %}} 
##  **Conversión de material no PBR a PBR**
En este ejemplo de código se muestra cómo convertir material en material PBR y, a continuación, guardar la escena 3D en el formato GLTF:

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
