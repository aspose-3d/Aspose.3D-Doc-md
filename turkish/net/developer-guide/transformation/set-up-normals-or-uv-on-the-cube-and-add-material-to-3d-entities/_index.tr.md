---
title: Set up normals or UV on the Cube and Add Material to 3D Entities
type: docs
weight: 20
url: /tr/net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Aspose içinde bir ağ üzerinde normaller veya uv verileri nasıl oluşturulur. 3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET geometrik şekillerdeki normalleri ve uv'yi yönetmeyi teklif eder. Bir ağ, her bir verteksin temel özelliklerini depolar, uzayda konumu ve normal, orijinal yüzeye dik bir vektör. Normal, sayıları gölgelendirmek için önemlidir. Normaller birim vektörleri olmalıdır. Çoğu örgü biçimi, ağın farklı poligonlarına uygulamak için 2 boyutlu bir doku haritasının hangi kısmının uygulanacağını göstermek için "açılmamış" ağının ayrı bir 2d gösterimi olan bir uv koordinatlarını da destekler.

{{% /alert %}} {{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](/3d/net/create-3d-mesh-and-scene/) and then point node to the Mesh geometry by [Creating a 3D Scene](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Create Normal ctors ectors**
Aydınlatma konusunda iyi bir görsel görünüme sahip olmak için, her vertex için normaller bilgilerini belirtmemiz, daha iyi bir ayrıntıya sahip olmamız gerekiyor, ayrıca normal ve dağınık haritayı da kullanabiliriz (gölge/speküler haritasını kullanabileceğinizden emin olun)-piksel başına normal/renk. Vertexelement tarafından normal veya vertex rengi gibi bir vertex bilgisi elde edilir. Aspose.3D vertex/polygon/edge noktalarını kontrol etmek için ekstra bilgileri haritalayabiliriz, vertex için normalleri tanımlamak için bir örnek:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Raw normal data
Vector4[] normals = new Vector4[]
{
    new Vector4(-0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258,-0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258,-0.577350258, 1.0)
};

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;
// Copy the data to the vertex element
elementNormal.Data.AddRange(normals);

{{< /highlight >}}

The 8 normal vektör, 8 kontrol noktasına doğrudan eşleştirilir, bir sonraki örnekte, biraz daha karmaşık bir senaryo göstereceğiz.
##  **Create UV ordinoordinates**
Here, sadece 4 UV koordinatlarını tanımladık, ancak endeksleri kullanarak 24 poligon dikeyine (poligon başına 6 yüz * 4 vertex) uyguladık.
Aspose.3D 5 haritalama modu sağlar:

- `ControlPoint` -her veri geometrinin kontrol noktasına eşleştirilir.
- `PolygonVertex` -veriler poligon'un vertex'ine eşleştirildi.
- `Polygon` -veriler çokgen ile eşleştirilir.
- `Edge` -veriler kenara yazılmıştır.
- `AllSame` -tüm geometriye bir veri eşleştirildi.



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// UVs
Vector4[] uvs = new Vector4[]
{
    new Vector4( 0.0, 1.0,0.0, 1.0),
    new Vector4( 1.0, 0.0,0.0, 1.0),
    new Vector4( 0.0, 0.0,0.0, 1.0),
    new Vector4( 1.0, 1.0,0.0, 1.0)
};

// Indices of the uvs per each polygon
int[] uvsId = new int[]
{
    0,1,3,2,2,3,5,4,4,5,7,6,6,7,9,8,1,10,11,3,12,0,2,13
};

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();

// Create UVset
VertexElementUV elementUV = mesh.CreateElementUV(TextureMapping.Diffuse, MappingMode.PolygonVertex, ReferenceMode.IndexToDirect);
// Copy the data to the UV vertex element 
elementUV.Data.AddRange(uvs);
elementUV.Indices.AddRange(uvsId);

{{< /highlight >}}
##  **Add Materials to 3D Objects**
Aspose.3D for .NET, geliştiricilerin doğru gölgeleme ve vurgular için gölgeleme algoritmasını kullanmasına izin verir. Phong, düğümün etkisini maskelemek için kullanabileceğimiz birkaç harita girişine sahiptir. Fiziksel olarak dayalı render (pbr) nesnelerin bazı fiziksel özelliklerini dikkate alır, bu tür bir yaklaşım gerçek dünyada olduğu gibi malzemelerin görünümünü sağlar.
###  **Cube için Texture ile Phong erial aterial**
Uhen Ucoordinates koordinatları kullanıma hazır, malzeme kullanarak örgü yüzeyine bir doku uygulayabiliriz. Only vertex rengi, yüzey detaylarını tarif edemez, bu da kullanılan malzemelerdir. Here, küp düğümüne bir Phong malzemesi eklemek için bir örnek:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
            
// Initialize cube node object
Node cubeNode = new Node("cube");

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
         
// Point node to the mesh
cubeNode.Entity = mesh;
            
// Add cube to the scene
scene.RootNode.ChildNodes.Add(cubeNode);
            
// Initiallize PhongMaterial object
PhongMaterial mat = new PhongMaterial();
            
// Initiallize Texture object
Texture diffuse = new Texture();
            
// The path to the documents directory.
            
// Set local file path
diffuse.FileName = RunExamples.GetOutputFilePath("surface.dds");

// Set Texture of the material
mat.SetTexture("DiffuseColor", diffuse);

// Embed raw content data to FBX (only for FBX and optional)
// Set file name
diffuse.FileName = "embedded-texture.png";
// Set binary content
diffuse.Content = File.ReadAllBytes(RunExamples.GetDataFilePath("aspose-logo.jpg"));

// Set color
mat.SpecularColor = new Vector3(Color.Red);

// Set brightness
mat.Shininess = 100;

// Set material property of the cube object
cubeNode.Material = mat;
            
// Save 3D scene in the supported file formats
scene.Save("MaterialToCube.fbx");

{{< /highlight >}}

We dağınık doku haritalama ve parlaklık parametresi ile speküler bir renk belirledi.
###  **Hyhycally hysically Based dering en( (PBR) erial aterial to a Box**
PBR plays a key role for the game engine visuals, with its efficient and realistic rendering of interactions between light and surface via attenuation of the brightness and scattering of reflected light. Developers can use Aspose.3D API to apply PBR material to 3D objects in a scene. This code example demonstrates to how to create a Box object, and then apply the PBR material.

**.NET, C#**

{{< highlight "java" >}}

 // initialize a scene

Scene scene = new Scene();

// initialize PBR material object

PbrMaterial mat = new PbrMaterial();

// an almost metal material

mat.MetallicFactor = 0.9;

// material surface is very rough

mat.RoughnessFactor = 0.9;

// create a box to which the material will be applied

var boxNode = scene.RootNode.CreateChildNode("box", new Box());

boxNode.Material = mat;

// save 3d scene into STL format

scene.Save(@"C:\3D\PBR_Material_Box_Out.stl", FileFormat.STLASCII);

{{< /highlight >}}
