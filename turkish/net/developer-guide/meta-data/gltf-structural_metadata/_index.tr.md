---
title: glTF Yapısal Meta Veri Örneği
type: docs
linkTitle: glTF Yapısal Meta Veri
description: Bu doküman sayfası, Aspose.3D for .NET kullanarak bir glTF dosyasından yapısal meta verileri nasıl okunacağını göstermektedir.
weight: 11
---

# glTF Dosyalarından Yapısal Meta Verileri Okuma

Bu örnek, Aspose.3D API'si kullanarak yapısal meta verileri, EXT_structural_metadata uzantısını içeren bir glTF dosyasından nasıl okunacağını göstermektedir.

## Kod Açıklaması

Aşağıdaki C# kodu, yapısal meta verilerle bir glTF sahnesini yükler, ardından özellik tabloları ve özellikleri hakkında bilgileri okur ve görüntüler:

```csharp
// Dosyadan EXT_structural_metadata ile glTF sahnesini yükle
var scene = Scene.FromFile("ComplexType.gltf");

// Sahneden yapısal meta verileri yükle
var metadata = StructuralMetadata.From(scene);
Console.WriteLine("Girdi glTF dosyasından yapısal meta verileri dökümü:");

// Meta verilerdeki tüm özellik tablolarını yinele
foreach (var propTable in metadata.PropertyTables)
{
    // Özellik tablosunun meta sınıfını al
    Console.WriteLine($"Özellik Tablosu {propTable.Name}, tür adı : {propTable.MetaClass.Name}");

    // Meta sınıfta tanımlanan tüm özellikleri yinele
    foreach (var propertyDefinition in propTable.MetaClass.Properties)
    {
        // EXT_structural_metadata'da tanımlanan özellik verisini al
        object property = propTable.Values[propertyDefinition.Name];
        
        // Özelliğin adı, türü ve değerini dök
        Console.WriteLine($"{propertyDefinition.Name} : {propertyDefinition.Type} = {property}");
    }
}
```

## Temel Kavramlar

### Yapısal Meta Veri
- `StructuralMetadata` sınıfı, EXT_structural_metadata uzantısında tanımlanan meta verilere erişim sağlar
- Bu uzantı, 3D nesneler hakkında semantik bilgi depolamaya olanak tanır
- Meta veri, sahnedeki nesneler için nitelikleri tanımlayan özellik tablolarını içerebilir

### Özellik Tabloları
- `PropertyTable` sınıfı tarafından temsil edilir
- Her tabloda şunlar bulunur:
  - Bir ad
  - Yapıyı tanımlayan bir meta sınıf
  - Gerçek özellik verilerini içeren değerler

### Meta Sınıflar
- `MetaClass` sınıfı tarafından tanımlanır
- Bir özellik tablosunun yapısını tanımlar
- Özellik tanımlarının bir koleksiyonunu içerir
- Her tanım şunları belirtir:
  - Özelliğin adı
  - Özelliğin türü
  - Diğer meta veri nitelikleri

### Özellik Erişimi
- Özellikler, bir özellik tablosunun `Values` sözlüğü aracılığıyla erişilir
- Anahtar, meta sınıfta tanımlanan özellik adıdır
- Değerler, mümkün olduğunda uygun türlere otomatik olarak dönüştürülür

Bu örnek, Aspose.3D'nin glTF dosyalarından yapısal meta verileri okumak ve işlemek için nasıl kullanılabileceğini göstermektedir ve geliştiricilerin 3D geometriyle birlikte depolanan zengin semantik bilgilere erişmelerini sağlar.