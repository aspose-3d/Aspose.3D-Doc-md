---
title: glTF Mesh Özellikleri Örneği
type: docs
linkTitle: glTF Mesh Özellikleri
description: Bu doküman sayfası, Aspose.3D for .NET kullanarak EXT_mesh_features ile bir glTF dosyası oluşturmayı göstermektedir.
weight: 10
---

# EXT_mesh_features ile glTF Dosyaları Oluşturma

Bu örnek, Aspose.3D API'si kullanarak EXT_mesh_features uzantısına sahip bir glTF dosyası oluşturma yöntemini göstermektedir.

## Kod Açıklaması

Aşağıdaki C# kodu, kontrol noktaları ve çokgenlerden oluşan bir ağ oluşturur ve ardından glTF dosyasına kaydetmeden önce kontrol noktalarına özellik kimlikleri ekler:

```csharp
// Bu örnek, EXT_mesh_features ile bir glTF dosyası oluşturacaktır
// Öncelikle bir ağ oluşturuyoruz
var mesh = new Mesh();

// Ağa kontrol noktaları (köşeler) ekleyin
// İlk dört nokta, y=1'de XY düzleminde bir kare oluşturur
mesh.ControlPoints.Add(new Vector4(0, 1, 0));  // Nokta 0
mesh.ControlPoints.Add(new Vector4(2, 1, 0));  // Nokta 1
mesh.ControlPoints.Add(new Vector4(2, 2, 0));  // Nokta 2
mesh.ControlPoints.Add(new Vector4(1, 2, 0));  // Nokta 3

// İkinci dört nokta, y=0'de XY düzleminde başka bir kare oluşturur
mesh.ControlPoints.Add(new Vector4(3, 0, 0));  // Nokta 4
mesh.ControlPoints.Add(new Vector4(4, 0, 0));  // Nokta 5
mesh.ControlPoints.Add(new Vector4(4, 1, 0));  // Nokta 6
mesh.ControlPoints.Add(new Vector4(3, 1, 0));  // Nokta 7

// Kontrol noktalarından üçgen yüzler (çokgenler) oluşturun
// İlk kare (noktalar 0-3) iki üçgene bölünmüştür
mesh.CreatePolygon(0, 1, 2);  // Üçgen 0-1-2
mesh.CreatePolygon(0, 2, 3);  // Üçgen 0-2-3

// İkinci kare (noktalar 4-7) de iki üçgene bölünmüştür
mesh.CreatePolygon(4, 5, 6);  // Üçgen 4-5-6
mesh.CreatePolygon(4, 6, 7);  // Üçgen 4-6-7

// Ardından, özellik kimliklerini depolamak için bir kullanıcı veri öğesi oluşturuyoruz
// Bu, özellik kimliklerini kontrol noktalarıyla ilişkilendirecektir
var featureId = (VertexElementUserData)mesh.CreateElement(
    VertexElementType.UserData,  // Öğe türü
    MappingMode.ControlPoint,   // Kontrol noktalarına uygulanır
    ReferenceMode.Direct        // Doğrudan eşleme (indeksli değil)
);

// Her kontrol noktasına özellik kimlikleri atayın
// İlk dört nokta kimlik 0'ı, sonraki dört kimlik 1'i alır
featureId.Data = new float[] { 0, 0, 0, 0, 1, 1, 1, 1 };

// EXT_mesh_features belirtimine uygun olan özel öznitelik adını ayarlayın
// _FEATURE_ID_<n> biçimi glTF ihracatçısı tarafından tanınır
featureId.Name = "_FEATURE_ID_0";

// Ağı bir glTF İkili (GLB) dosyasına kaydedin
// İhracatçı, otomatik olarak EXT_mesh_features uzantısı verilerini oluşturacaktır
// Çıkış dosyası için göreli yol kullanılarak
(new Scene(mesh)).Save("mesh_feature.glb");
```

## Temel Kavramlar

### Ağ Oluşturma
- `Mesh` sınıfı, çokgenli ağ geometrisini temsil eder
- Kontrol noktaları, ağın köşelerini tanımlar
- `CreatePolygon` yöntemi, kontrol noktaları arasında üçgen yüzler oluşturur

### Özellik Kimlikleri
- Özellik kimlikleri, bir ağ içindeki geometrinin gruplandırılmasını sağlar
- `VertexElementUserData` ile özel adlandırma kuralı kullanılarak uygulanır
- `_FEATURE_ID_0`, bu bir özellik kimlikleri akışını gösterir
- Artan indekslerle birden fazla özellik kimlikleri akışı oluşturulabilir

### Veri Ataması
- Özellik kimlikleri, kayan nokta değerleri olarak depolanır
- Her kontrol noktasına karşılık gelen bir özellik kimlikleri değeri atanır
- Bu örnekte, 0 ve 1 olmak üzere iki farklı özellik kimliği kullanıyoruz

### Dosya İhracatı
- GLB biçimine kaydetmek, EXT_mesh_features dahil olmak üzere tüm özellikleri korur
- Aspose.3D, uzantı oluşturmayı otomatik olarak yönetir
- Sonuçtaki dosya, ağ özellikleriyle ilgili meta veriler içerir
- Göreceli yollar kullanmak, kodu daha taşınabilir hale getirir ve farklı ortamlarda daha kolay çalışmasını sağlar

Bu örnek, Aspose.3D'nin, gelişmiş 3D veri gösterimi için EXT_mesh_features uzantısını kullanan glTF dosyaları oluşturmak için nasıl kullanılabileceğini göstermektedir.