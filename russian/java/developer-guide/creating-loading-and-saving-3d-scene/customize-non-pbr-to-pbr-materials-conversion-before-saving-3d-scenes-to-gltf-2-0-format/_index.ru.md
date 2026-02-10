---
title: Настройте преобразование материалов без PBR в PBR перед сохранением сцен 3D в формат GLTF 2,0
type: docs
weight: 50
url: /ru/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Класс Сцена Aspose.3D for Java API представляет сцену 3D, и разработчики могут построить сцену 3D, добавив различные сущности.
---
{{% alert color="primary" %}} 

Класс `Scene` Aspose.3D for Java API представляет сцену 3D, и разработчики могут построить сцену 3D, добавив различные сущности. GLTF 2,0 поддерживает только материалы PBR (физический рендеринг), Aspose.3D API внутренне преобразует материалы, не являющиеся PBR, в материалы PBR перед экспортом в GLTF 2,0 (материалы в сцене останутся неизменными во время экспорта), и разработчики могут предоставить пользовательскую функцию преобразования для переопределения поведения по умолчанию.

{{% /alert %}} 
##  **Преобразование материала Non-PBR в PBR**
Этот пример кода демонстрирует, как преобразовать материал в материал PBR, а затем сохранить сцену 3D в формате GLTF:

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
