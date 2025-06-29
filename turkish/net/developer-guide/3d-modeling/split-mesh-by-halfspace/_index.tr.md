---
title: "Aspose.3D'de Yarım Uzay ile Ağı Bölmek Nasıl Yapılır"
type: docs
linkTitle: "Yarı Uzay ile Mesh'i Böl"
description: "Aspose.3D'de Yarım Alan düzlemleri kullanarak 3B mesh'leri nasıl böleceğinizi öğrenin"
weight: 10
---

# Aspose.3D'de YarıÇözgi ile Ağları Bölme

Bu eğitim, Aspose.3D'yi kullanarak yarıçözgi düzlemleriyle ağ bölme işlemleri nasıl yapılacağını göstermektedir. Bu teknik, 3B modelin belirli bölümlerini uzamsal kriterlere göre çıkarmak için kullanışlıdır.

## YarıÇözgi İşlemlerini Anlama

Yarıçözgi, bir düzlemle bölünen sonsuz bir alanı temsil eder. Aspose.3D'nin boolean işlemlerini birleştirdiğinde, tanımlı düzlemin bir tarafında bulunan bir ağın belirli bölümlerini çıkarmayı sağlar.

### Temel Kavramlar:
- **YarıÇözgi**: Bir düzlemle bölünen sonsuz bir alanı temsil eder
- **Boolean İşlemleri**: YarıÇözgiye göre ağ bölümlerini çıkarmak için kullanılır
- **Düzlem Denklemi**: (a,b,c) normal vektör olarak tanımlanır ax + by + cz + d = 0 şeklinde tanımlanır
- **Pozitif Taraf**: Düzlem normalinin işaret ettiği uzayın bölümü

## Kod Örneği: YarıÇözgi ile Bir Ağı Bölme

Aşağıdaki C# kodu, basit bir kutu ağı oluşturmayı ve bir yarıçözgi düzlemi kullanarak bölmeyi göstermektedir:

```csharp
using System;
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;
using Aspose.ThreeD.Utilities;

class MeshBooleanWithHalfSpace
{
    public static void Execute()
    {
        // Yeni bir 3B sahnesi oluştur
        Scene scene = new Scene();
        
        // Varsayılan 2x2x2 boyutlarında bir kutu ağı oluştur
        Mesh boxMesh = (new Box()).ToMesh();
        Node boxNode = scene.RootNode.CreateChildNode("Box", boxMesh);
        
        // YarıÇözgi kesme düzlemi oluştur
        HalfSpace halfSpace = new HalfSpace();
        
        // Düzlem denklemini tanımlayın: ax + by + cz + d = 0
        // Z-yönünde işaret eden düzlem normalini kullanarak
        halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
        
        // YarıÇözgi'yi konumlandırın (düğüm ve dönüşüm oluşturun)
        Node halfSpaceNode = scene.RootNode.CreateChildNode("HalfSpace", halfSpace);
        halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);  // z=0.5'te konumlandır
        
        // Boolean bölme işlemi gerçekleştir
        Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
        
        // Sonucu sahneye ekle ve kaydet
        scene.RootNode.CreateChildNode("SplitResult", splitResult.Entity);
        scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
        
        Console.WriteLine("YarıÇözgi ile ağ bölme işlemi başarıyla tamamlandı.");
    }
}
```

## Kod Açıklaması

### Namespace Gereksinimleri
```csharp
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;  // HalfSpace ve BooleanOperator sınıflarını içerir
using Aspose.ThreeD.Utilities; // Vector3 ve Plane yardımcı sınıflarını içerir
```

### Geometriyi Oluşturma
1. **Sahne Başlatma**: `Scene scene = new Scene();`
2. **Kutu Oluşturma**: `(new Box()).ToMesh()` standart bir küp oluşturur
3. **Düğüm Hiyerarşisi**: Ağ, bir alt düğüm aracılığıyla sahneye eklenir

### Kesme Düzlemini Tanımlama
1. **Düzlem Tanımı**:
   ```csharp
   halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
   ```
   - z=0'da yatay XY düzlemi oluşturur
   - (0,0,1) normal vektörü yukarı doğru işaret eder

2. **Konumlandırma**:
   ```csharp
   halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);
   ```
   - Kesme düzlemini z=0.5'e taşır
   - Korunan ağ bölümünü etkiler

### İşlemi Gerçekleştirme
```csharp
Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
```
- Düzlemin pozitif tarafındaki ağ bölümünü döndürür
- Sonuç düğüm hiyerarşisine geri eklenir

### Sonucu Kaydetme
```csharp
scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
```
- Desteklenen formatlar arasında OBJ, STL, FBX, GLTF ve daha fazlası bulunur
- Sadece bölünen parça kaydedilir, orijinal ağ değil

## İşlemi Görselleştirme

### Orijinal Kutu Boyutları:
- (-1,-1,-1)'den (1,1,1)'e kadar uzanır
- Köken noktasında merkezlenmiştir

### Düzlem z=0.5'te olduğunda:
- z > 0.5 (kutu üst kısmı) olan kısım korunur
- z < 0.5 (kutu alt kısmı) olan kısım atılır

## Gelişmiş Kullanım

### Kesimin Her İki Tarafını Alma
```csharp
// Orijinal bölme (pozitif taraf)
Node positiveFragment = BooleanOperator.Split(boxNode, halfSpaceNode);

// Negatif taraf için düzlemi ters çevir
halfSpace.Plane = new Plane(new Vector3(0, 0, -1), 0);
Node negativeFragment = BooleanOperator.Split(boxNode, halfSpaceNode);
```

### Kesme Düzlemini Ayarlama
```csharp
// Farklı yönlendirme - açılı kesim
halfSpace.Plane = new Plane(new Vector3(0.707, 0, 0.707), 0);
halfSpaceNode.Transform.Translation = new Vector3(0, 0, 1);
```

Bu uygulama, Aspose.3D'nin yarıçözgi düzlemleri kullanarak ağ bölme yeteneklerinin temel işlevselliğini göstermektedir ve 3B geometrinin uzamsal kriterlere göre hassas bir şekilde çıkarılmasını sağlamaktadır.