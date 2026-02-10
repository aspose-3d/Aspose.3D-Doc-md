---
title: تخصيص تحويل مواد غير PBR إلى PBR قبل توفير 3D مشاهد إلى تنسيق GLTF 2.0
type: docs
weight: 50
url: /ar/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: فئة المشهد لـ Aspose.3D for Java API يمثل مشهد 3D ويمكن للمطورين إنشاء مشهد 3D بإضافة كيانات مختلفة.
---
{{% alert color="primary" %}} 

فئة `Scene` من Aspose.3D for Java API تمثل مشهد 3D ويمكن للمطورين إنشاء مشهد 3D بإضافة كيانات مختلفة. يدعم GLTF 2.0 فقط مواد PBR (تقديم قائم على أساس مادي) ، Aspose. يحول 3D API داخليًا المواد غير المعالجة بالكمبيوتر إلى مواد PBR قبل التصدير إلى GLTF 2.0 (ستظل المواد في المشهد دون تغيير أثناء التصدير) ، ويمكن للمطورين توفير وظيفة تحويل مخصصة لتجاوز السلوك الافتراضي.

{{% /alert %}} 
##  **Non-PBR إلى PBateraterateron**
This code example demonstrates how to convert material to PBR material, and then saves 3D scene in the GLTF format:

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
