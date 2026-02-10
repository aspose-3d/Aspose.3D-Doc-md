---
title: Split Mesh
type: docs
weight: 10
url: /tr/java/split-mesh/
description: Aspose.3D for Java API has support to split all meshes of a scene into several sub meshes per material. The SplitMesh method will not split a mesh of the scene, if it has been assigned a single material. It can be achieved by using Aspose.3D for Java API.
---
##  **Cene plit cene cene er erial aterial tüm shes eshes**
Aspose.3D for Java API has support to split all meshes of a scene into several sub meshes per material. The SplitMesh method will not split a mesh of the scene, if it has been assigned a single material. It can be achieved by using Aspose.3D for Java API.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum, ağ bölme algoritmasında kullanılan veri politikasını belirtir, iki politikayı destekler, alt ağlar veya her bir alt ağ arasındaki verileri paylaşır (sadece kullanılan veriler).

{{% /alert %}} 

The kod örneği aşağıda malzeme başına bir sahnenin tüm ağlarını böler. Each alt ağ aynı doğrudan verileri paylaşır ve sadece endekslerde farklılık gösterir.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "test.fbx";
// Load a 3D file
Scene scene = new Scene(MyDir);
// Split all meshes
PolygonModifier.splitMesh(scene, SplitMeshPolicy.CLONE_DATA);
// Save file
MyDir = RunExamples.getDataDir() + RunExamples.getOutputFilePath("test-splitted.fbx");
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
##  **Erial plit a erial esh erial pecicithe erial aterial**
Aspose.3D for Java API malzemeyi manuel olarak belirterek bir ağı bölmeyi desteklemektedir. Bölünmüş örgü seçeneği ayrı nesneler oluşturur ve her alt örgü sadece bir malzeme kullanır.
###  **Box Split Mesh**
Bu yardım konusu, kodu kapsamlı ve kısa tutmak için kutunun bir örgü oluşturur. Geliştiriciler, bu yardım konusu hakkında manuel olarak bir ağ oluşturabilirler: [3D küp mesh oluşturun](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Ayrıca, bir kutu 6 uçak ile oluşur ve her uçak bir alt ağ haline gelir. Aşağıdaki kod örneği, malzemeyi manuel olarak belirterek ilkel bir ağ oluşturur.

{{< highlight "java" >}}
// Create a mesh of box(A box is composed by 6 planes)
Mesh box = (new Box()).toMesh();
// Create a material element on this mesh
VertexElementMaterial mat = (VertexElementMaterial) box.createElement(VertexElementType.MATERIAL, MappingMode.POLYGON, ReferenceMode.INDEX);
// and specify different material index for each plane
mat.setIndices(new int[]{0, 1, 2, 3, 4, 5});
// Now split it into 6 sub meshes, we specified 6 different materials on each plane, each plane will become a sub mesh.
// We used the CloneData policy, each plane will has the same control point information or control point-based vertex element information.
Mesh[] planes = PolygonModifier.splitMesh(box, SplitMeshPolicy.CLONE_DATA);
mat.getIndices().clear();
mat.setIndices(new int[]{0, 0, 0, 1, 1, 1});
// Now split it into 2 sub meshes, first mesh will contains 0/1/2 planes, and second mesh will contains the 3/4/5th planes.
// We used the CompactData policy, each plane will has its own control point information or control point-based vertex element information.
planes = PolygonModifier.splitMesh(box, SplitMeshPolicy.COMPACT_DATA);
{{< /highlight >}}
