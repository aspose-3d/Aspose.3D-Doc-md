---
description: "Bu belge sayfası, Aspose.3D for .NET kullanarak bir IFC dosyasından özelliklerin nasıl okunacağını gösterir."
linkTitle: "IFC Özellik Desteği"
title: "IFC Özellik Desteği"
type: docs
weight: 14
---
## Genel Bakış

IFC Property Support, Aspose.3D'de geliştiricilerin IFC dosyalarında tanımlı özellik setlerini ve eleman miktarlarını okuyabilmelerini sağlayan bir özelliktir. Bu özellikler `IFCPROPERTYSET` ve `IFCELEMENTQUANTITY` varlıkları içinde saklanır ve `A3DObject.GetProperty` yöntemi aracılığıyla erişilebilir.

## IFC Property Support Nedir?

IFC şemasında, yapı elemanlarının ilişkili özellik setleri (`IFCPROPERTYSET`) ve eleman miktarları (`IFCELEMENTQUANTITY`) bulunabilir. Aspose.3D, bunları jenerik bir özellik arayüzüne eşler ve `A3DObject.GetProperty(string propertyName)` üzerinden sunar. Böylece 3D modelden doğrudan yangın dayanımı, ısı geçirgenliği veya malzeme miktarları gibi değerler alınabilir.

## Neden IFC Property Support Kullanılmalı?

* IFC dosyasını elle ayrıştırmadan zengin anlamsal verilere erişim.
* Maliyet tahmini, uyumluluk kontrolü veya veri dışa aktarımı gibi sonraki süreçlerin etkinleştirilmesi.
* Geometrik ve geometrik olmayan bilgilerin tek bir iş akışında birleştirilmesi.

## Aspose.3D Desteği

Aşağıdaki C# örneği, bir IFC dosyasını nasıl yükleyeceğinizi ve bir özelliği nasıl okuyacağınızı gösterir:

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");

// Belirli bir elemanı bulun, örn. bir duvar
var wallNode = scene.RootNode.Children.FirstOrDefault(n => n.Name == "Wall_123");

// Bir özellik değerini alın
if (wallNode != null)
{
    // IFC dosyasında tanımlı özellik adı
    var fireRating = wallNode.GetProperty("ifc:FireRating");
    Console.WriteLine($"Fire Rating: {fireRating}");

    // Eleman miktarı örneği
    var volume = wallNode.GetProperty("ifc:GrossVolume");
    Console.WriteLine($"Gross Volume: {volume}");
}
```

### Notlar

* IFC dosyasında tanımlı özellik adları, yerel özelliklerle çakışmayı önlemek için `ifc:` önekiyle başlar.
* Özellik adları büyük/küçük harfe duyarlıdır ve IFC dosyasında tanımlı isimlerle tam olarak eşleşmelidir.  
* `GetProperty` bir `object` döndürür; gerektiğinde uygun tipe (örn. `double`, `string`) dönüştürülmelidir.  
* Bu örnek kod, `Node` üzerinden özellik alımını gösterir; ancak `A3DObject`'in herhangi bir türevi `GetProperty` kullanılabilir.
* Bir özellik mevcut değilse, `GetProperty` `null` döndürür.

## Referanslar

* [Resmi Aspose.3D IFC belgelerine bağlantı](/3d/net/supported-file-formats/ifc)
* [`Aspose.ThreeD.A3DObject`](https://reference.aspose.com/3d/net/aspose.threed/a3dobject/) bağlantısı
* `IFCPROPERTYSET` ve `IFCELEMENTQUANTITY` için IFC spesifikasyonu