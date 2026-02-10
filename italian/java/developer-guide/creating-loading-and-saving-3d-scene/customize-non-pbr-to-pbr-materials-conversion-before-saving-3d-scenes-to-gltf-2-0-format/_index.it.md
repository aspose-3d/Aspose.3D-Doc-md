---
title: Personalizza la conversione dei materiali da PBR a PBR prima di salvare 3D scene in GLTF 2.0 Formato
type: docs
weight: 50
url: /it/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La classe Scene di Aspose.3D for Java API rappresenta una scena di 3D e gli sviluppatori possono creare una scena di 3D aggiungendo varie entità.
---
{{% alert color="primary" %}} 

La classe `Scene` di Aspose.3D for Java API rappresenta una scena 3D e gli sviluppatori possono creare una scena 3D aggiungendo varie entità. GLTF 2.0 supporta solo materiali PBR (Rendering basato sulla fisica), Aspose.3D API converte internamente materiali non PBR in materiali PBR prima di esportare in GLTF 2.0 (i materiali nella scena rimarranno invariati durante l'esportazione) e gli sviluppatori possono fornire la funzione di conversione personalizzata per sovrascrivere il comportamento predefinito.

{{% /alert %}} 
##  **Conversione del materiale da non PBR a PBR**
Questo esempio di codice mostra come convertire il materiale in materiale PBR e quindi salvare la scena 3D nel formato GLTF:

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
