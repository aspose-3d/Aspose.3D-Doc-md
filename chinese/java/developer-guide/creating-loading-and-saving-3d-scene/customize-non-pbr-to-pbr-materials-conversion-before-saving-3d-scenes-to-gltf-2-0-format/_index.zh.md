---
title: 在将 3D 个场景保存为 GLTF 个2.0格式之前，自定义非PBR到PBR材质的转换
type: docs
weight: 50
url: /zh/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Aspose.3D for Java API 的场景类表示 3D 场景，开发人员可以通过添加各种实体来构建 3D 场景。
---
{{% alert color="primary" %}} 

Aspose.3D for Java API 的 `Scene` 类表示 3D 场景，开发人员可以通过添加各种实体来构建 3D 场景。GLTF 2.0仅支持PBR (基于物理的渲染) 材质，Aspose.3D API 将非PBR材质内部转换为PBR材质，然后导出为 GLTF 2.0 (导出时场景中的材质将保持不变)，并且开发人员可以提供自定义转换函数来覆盖默认行为。

{{% /alert %}} 
##  **非PBR到PBR材料转换**
此代码示例演示如何将材质转换为PBR材质，然后以 GLTF 格式保存 3D 场景:

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
