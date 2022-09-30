---
title: Aspose.3D for Java 18.7 - July 2018
type: docs
weight: 60
url: /tr/java/aspose-3d-for-java-18-7-july-2018/
---
{{% alert color="primary" %}} 

This sayfası için sürüm notları içerir[Aspose.3D for Java 18.7](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.7/).

{{% /alert %}} 
## **Ther ther vements mprovements ve Changes**

|**Summary**|**Category**|
|:- |:- |
|Add Draco 2.2 İthalat desteği|Ew ew Feature|
|Add Draco 2.2 İhracat desteği|Ew ew Feature|
|Draco sıkıştırma ile 07mport glTF dosyaları|Ew ew Feature|

## **Public API ve Backwards uyumlu Changes**
Lease lease API halka yapılan herhangi bir değişiklik listesini, Aspose.3D for Java API için yapılan geri dönüşsüz uyumlu değişimin yanı sıra eklenen, yeniden adlandırılmış, kaldırılmış veya kullanımdan kaldırılmış üyelerin listesini görüntüleyin. If listelenen herhangi bir değişiklik hakkında endişeleriniz var, lütfen[Aspose.3D destek forumu](https://forum.aspose.com/c/3d).

## **API değişiklikleri:**

**3 üye sınıf com.aspose.threed.Property kaldırıldı:**

{{< highlight "java" >}}

     public void com.aspose.threed.Property.setExtraData(java.lang.String);

    public java.lang.String com.aspose.threed.Property.getExtraData();

    public int com.aspose.threed.Property.getFlags();

{{< /highlight >}}

These .NET sürümündeki değişiklikleri senkronize etmek için kaldırılır. (They Aspose.3D for .NET 18.2 tarihinden beri kaldırılması planlanıyor)

**Sınıf com.aspose.threed. bjbjLoad: ptions:**

{{< highlight "java" >}}

     public boolean com.aspose.threed.ObjLoadOptions.getNormalizeNormal();

    public void com.aspose.threed.ObjLoadOptions.setNormalizeNormal(boolean);

{{< /highlight >}}

Yükleme sırasında normal vektörü normalleştirmek için ets ets veya ayarlar, varsayılan değer doğrudur.

**Sample kodu:**

{{< highlight "java" >}}

         Scene scene = new Scene();

        ObjLoadOptions opt = new ObjLoadOptions();

        opt.setNormalizeNormal(false);

        scene.open("test.obj", opt);

{{< /highlight >}}

This obj dosyasını yükleyecek ve normal vektörleri normalize etmeyecektir, eski sürüm obj dosyası yüklendiğinde normal vektörleri normalleştirecektir.
