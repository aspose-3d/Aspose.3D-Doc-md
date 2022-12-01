---
title: Licensing
description: Python via .NET için Aspose.3D, satın alma için farklı planlar sağlar veya Lree Trial ve Licensing ve Sub. politikalarını kullanarak değerlendirme için 30 günlük Temporary License sunar."
type: docs
weight: 80
url: /tr/python-net/licensing/
---
Stimes times, sistemi daha iyi incelemek için, mümkün olduğunca hızlı bir şekilde koda dalmak istersiniz. To bunu kolaylaştırıyor, Aspose.3D satın alma için farklı planlar sunuyor veya değerlendirme için bir Free Trial ve 30 günlük bir empemporary License sunuyor.

{{% alert color="primary" %}}

Note, ürünlerimizi nasıl değerlendireceğiniz, uygun şekilde lisanslanacağınız ve satın alacağınız konusunda size rehberlik eden bir dizi genel politika ve uygulama bulunmaktadır. You onları bulabilir["Purchase Policies ve FAQ"](https://purchase.aspose.com/policies)Bölüm.

{{% /alert %}}

## **E07ate Aspose.3D**
You, değerlendirme için Aspose.3D 'ü kolayca indirebilir. The değerlendirme paketi satın alınan paketle aynıdır. To değerlendirme sürümü, lisansı uygulamak için birkaç kod satırı ekledikten sonra lisanslanır.

## **Edeğerleme Version imitation imitation**
The değerlendirme sürümü aşağıdakiler hariç tüm özellikleri sağlar:

- Users sadece 50 3D belgesini Scene 'e açabilir/içe aktarabilir.
- Ach ach düğümü en fazla 5 çocuk düğümüne sahip olamaz.
- Ach ach düğümünün 2'den fazla ekli varlığa sahip olamaz.
- Each geometrisi 2'den fazla ekli vertex elementine sahip olamaz.
- Each düğümü 1'den fazla malzemeye sahip olamaz.
- Users sadece en fazla 50 3D belgesini Scene 'e kaydedebilir.
- Users ayrıca işlenmiş görüntülerde ve diğer tüm çıktı dosyalarında bir değerlendirme filigranı görecektir.

{{% alert color="primary" %}} 
If uygun bir lisans olmadan Aspose.3D kullanıyorsunuz, kullanım lisanssız kısıtlamalara ulaştığında bir `aspose.threed.TrialException` tetikleyebilir, istisnayı şu şekilde kapatabilirsiniz:

* [Tam özellikli bir lisans](https://purchase.aspose.com/buy).
* Request 30 günlük geçici bir lisans, lütfen [How to get a Temporary License?](https://purchase.aspose.com/temporary-license) Fveya daha fazla bilgi.
* Manually 'try cene.open/save' üzerinde bir 'try/except' bloğu kullanın, bu istisna sadece bir bildirim, sahne yükleme/tasarrufu etkilemez görmezden gelir.

{{% /alert %}} 


## **LLLicense**
You Aspose.3D Python via .NET için bir değerlendirme sürümünü kolayca indirebilir[İndirme sayfası](https://pypi.org/project/aspose.3d/). The değerlendirme sürümü kesinlikle sağlar**Aynı yetenekler**Aspose.3D lisanslı versiyonu olarak. Furthermore, değerlendirme sürümü sadece bir lisans satın aldıktan sonra lisanslı hale gelir ve lisansı uygulamak için birkaç kod satırı ekler.

The lisansı, ürün adı, geliştiricilerin sayısı, abonelik son kullanma tarihi ve benzeri gibi ayrıntıları içeren düz bir metin XML dosyasıdır. The dosyası dijital olarak imzalanmış, bu yüzden dosyayı değiştirmeyin. Even dosyanın içeriğine ekstra bir hat kırılmasının yanlışlıkla eklenmesi bunu geçersiz kılacaktır.

To değerlendirme sürümü ile ilişkili sınırlamaları önlemek, kullanmadan önce bir lisans ayarlamanız gerekir**Aspose.3D**. You sadece uygulama veya işlem başına bir kez lisans ayarlamak için gereklidir.

## PururLicense

Fter fter satın alma, lisans dosyasını veya akışını uygulamanız gerekir. This bölümü, bunun nasıl yapılabileceğine dair seçenekleri ve bazı yaygın sorularla ilgili yorumları açıklar.

{{% alert color="primary" %}}

You lisansı ayarlamanız gerekiyor:
* Uygulama alanı başına sadece bir kez
* Başka Aspose.3D sınıfları kullanmadan önce

{{% /alert %}}

{{% alert color="primary" %}}

You fiyatlandırma bilgilerini bulabilir[“Pricing formation nformation”](https://purchase.aspose.com/pricing/3d/family)Sayfa.

{{% /alert %}}

### **Python via .NET için Aspose.3D yılında Letting bir License**

Licenses çeşitli konumlardan uygulanabilir:

* Explicit yolu
* Python via .NET için Aspose.3D numaralı python komut dosyasını içeren The klasörü
* Stream
* As a Metered License-yeni bir lisans mekanizması

{{% alert color="primary" %}}

Bir bileşeni lisanslamak için `set_license` yöntemini kullanın.

Calling `set_license` birden fazla kez zararlı değildir, sadece işlemci süresini boşa harcar.

{{% /alert %}}

In aşağıdaki bölümler, lisansı ayarlamak için kullanılan iki ortak yöntemi tanımlayacağız.

#### **Applying a License sing sing a File**
To bir lisans ayarlamanın en kolay yöntemi, lisans dosyasını Python için Aspose.3D numaralı python komut dosyasını içeren aynı klasöre yerleştirmenizi ve yolu olmayan sadece dosya adını belirtmenizi gerektirir.

Tkod snippet bir lisans dosyası ayarlamak için kullanılır:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license("Aspose.3D.lic")
```

When `set_license` yöntemini arayarak, lisans adı lisans dosyanızla aynı olmalıdır. Fveya örnek, lisans dosya adını "Aspose.3D.lic. xml" olarak değiştirebilirsiniz. Then, kodunuzda, yeni lisans adını (Aspose.3D.lic. xml) Set. icense yöntemine geçmelisiniz.

#### **Bir treatream gelen bir License pplying**
You bir akımdan lisans yükleyebilir.

Kod parçacığı bir akımdan bir lisans uygulamak için kullanılır:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license(stream)
```

#### Atered tered etered License

Aspose.3D, geliştiricilerin ölçülü bir anahtar uygulamasına izin verir. This yeni bir lisans mekanizmasıdır.

The yeni lisans mekanizması mevcut lisans yöntemi ile birlikte kullanılacaktır. 07API özelliklerinin kullanımına göre faturalandırılmasını isteyen hortum müşterileri, tered etered cenicensing'i kullanabilir.

Bu tür bir lisans almak için gerekli tüm adımları tamamladıktan sonra, lisans dosyası değil, anahtarları alacaksınız. Tonun ölçülü anahtarı, bu amaçla özel olarak tanıtılan `Metered` sınıfı kullanılarak uygulanabilir.

Kod örneğini takip eden T, ölçülü kamu ve özel anahtarların nasıl ayarlanacağını gösterir:

```py
import aspose.threed as a3d

# Create an instance of CAD Metered class
metered = a3d.Metered()

# Access the set_metered_key property and pass public and private keys as parameters
metered.set_metered_key("*****", "*****")

# Get metered data amount before calling API
amountbefore = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed Before: " + str(amountbefore))

# Load the scene from disk.
scene = a3d.Scene.from_file("3D Model.fbx")
# Save as pdf
scene.save("out_pdf.pdf", a3d.FileFormat.PDF)

# Get metered data amount After calling API
amountafter = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed After: " + str(amountafter))
```

{{% alert color="primary" %}}

Lease M, tered etered lisansının doğru kullanımı için sabit bir Internet bağlantısına sahip olmanız gerektiğini unutmayın, çünkü tered etered mekanizması doğru hesaplamalar için hizmetlerimizle sürekli etkileşimi gerektirir. Fveya daha fazla detay, bakın[“Tered etered Licensing FAQ”](https://purchase.aspose.com/faqs/licensing/metered)Bölüm.

{{% /alert %}}



