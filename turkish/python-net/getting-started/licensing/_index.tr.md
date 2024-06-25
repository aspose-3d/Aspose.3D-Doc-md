---
title: Licensing
description: Aspose.3D for Python via .NET satın alma için farklı planlar sağlar veya Licensing ve abonelik politikalarını kullanarak değerlendirme için ücretsiz deneme ve 30 günlük geçici lisans sunar
type: docs
weight: 80
url: /tr/python-net/licensing/
---
Sometimes, in order to study the system better, you want to dive into the code as fast as possible. To make this easier, Aspose.3D provides different plans for purchase or offers a Free Trial and a 30-day Temporary License for evaluation.

{{% alert color="primary" %}}

Ürünlerimizi nasıl değerlendireceğiniz, uygun şekilde lisanslanacağınız ve satın alacağınız konusunda size rehberlik eden bir dizi genel politika ve uygulama olduğunu unutmayın. Onları ["Purchase Policies ve FAQ"](https://purchase.aspose.com/policies) bölümünde bulabilirsiniz.

{{% /alert %}}

##  **Evaluate Aspose.3D**
You can easily download Aspose.3D for evaluation. The evaluation package is the same as the purchased package. The evaluation version simply becomes licensed after you add a few lines of code to apply the license. 

##  **Edeğerleme Version imitation imitation**
The değerlendirme sürümü aşağıdakiler hariç tüm özellikleri sağlar:

- Kullanıcılar sadece 50 3D belgelerini bir sahneyi açabilir/içe aktarabilir.
- Ach ach düğümü en fazla 5 çocuk düğümüne sahip olamaz.
- Ach ach düğümünün 2'den fazla ekli varlığa sahip olamaz.
- Each geometrisi 2'den fazla ekli vertex elementine sahip olamaz.
- Each düğümü 1'den fazla malzemeye sahip olamaz.
- Kullanıcılar sadece bir sahne için en fazla 50 3D belgesini kaydedebilir.
- Users ayrıca işlenmiş görüntülerde ve diğer tüm çıktı dosyalarında bir değerlendirme filigranı görecektir.

{{% alert color="primary" %}} 
If you're using Aspose.3D without a proper license, there could trigger an `aspose.threed.TrialException` when the usage reached the unlicensed restrictions, you can turn the exception off by:

* [Tam özellikli bir lisans satın alın](https://purchase.aspose.com/buy).
* Request a 30 days temporary license, please refer to [How to get a Temporary License?](https://purchase.aspose.com/temporary-license) For more information.
* Manually use a `try/except` block on `Scene.open/save`, this exception is just a notification, ignore it will not affect the scene loading/saving.

{{% /alert %}} 


##  **LLLicense**
Aspose.3D for Python via .NET 'lık bir değerlendirme sürümünü [İndirme sayfası](https://pypi.org/project/aspose.3d/) 'dan kolayca indirebilirsiniz. Değerlendirme sürümü kesinlikle sağlar**Aynı yetenekler**Aspose lisanslı versiyonu olarak. 3D. Ayrıca, değerlendirme sürümü, bir lisans satın aldıktan ve lisansı uygulamak için birkaç kod satırı ekledikten sonra lisanslanır.

The lisansı, ürün adı, geliştiricilerin sayısı, abonelik son kullanma tarihi ve benzeri gibi ayrıntıları içeren düz bir metin XML dosyasıdır. The dosyası dijital olarak imzalanmış, bu yüzden dosyayı değiştirmeyin. Even dosyanın içeriğine ekstra bir hat kırılmasının yanlışlıkla eklenmesi bunu geçersiz kılacaktır.

To değerlendirme sürümü ile ilişkili sınırlamaları önlemek, kullanmadan önce bir lisans ayarlamanız gerekir**Aspose.3D**. You sadece uygulama veya işlem başına bir kez lisans ayarlamak için gereklidir.

## PururLicense

Fter fter satın alma, lisans dosyasını veya akışını uygulamanız gerekir. This bölümü, bunun nasıl yapılabileceğine dair seçenekleri ve bazı yaygın sorularla ilgili yorumları açıklar.

{{% alert color="primary" %}}

You lisansı ayarlamanız gerekiyor:
* Uygulama alanı başına sadece bir kez
* Başka bir Aspose kullanmadan önce. 3D sınıfları

{{% /alert %}}

{{% alert color="primary" %}}

Fiyatlandırma bilgilerini [“Pricing formation nformation”](https://purchase.aspose.com/pricing/3d/family) sayfasında bulabilirsiniz.

{{% /alert %}}

###  **Setting a License in Aspose.3D for Python via .NET**

Licenses çeşitli konumlardan uygulanabilir:

* Explicit yolu
* Aspose.3D for Python via .NET olarak adlandırılan python komut dosyasını içeren klasör
* Akış
* Ölçülü bir lisans olarak-yeni bir lisans mekanizması

{{% alert color="primary" %}}

Bir bileşeni lisanslamak için `set_license` yöntemini kullanın.

Calling `set_license` multiple times is not harmful, it just wastes processor time.

{{% /alert %}}

In aşağıdaki bölümler, lisansı ayarlamak için kullanılan iki ortak yöntemi tanımlayacağız.

####  **Applying a License sing sing a File**
Bir lisansın ayarlanması için en kolay yöntem, lisans dosyasını Aspose olarak adlandırılan python komut dosyasını içeren aynı klasöre yerleştirmenizi gerektirir. 3D için Python ve sadece dosya adını yolu olmadan belirtin.

Tkod snippet bir lisans dosyası ayarlamak için kullanılır:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license("Aspose.3D.lic")
```

`set_license` yöntemini ararken, lisans adı lisans dosyanızla aynı olmalıdır. Örneğin, lisans dosya adını "Aspose.3D.lic.xml" olarak değiştirebilirsiniz. Daha sonra, kodunuzda, yeni lisans adını (Aspose.3D.lic.xml) setlicense yöntemine geçmelisiniz.

####  **Bir treatream gelen bir License pplying**
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

Aspose.3D, geliştiricilerin ölçülü bir anahtar uygulamasına izin verir. Bu yeni bir lisans mekanizması.

The new licensing mechanism will be used along with the existing licensing method. Those customers who want to be billed based on the use of API features can use the Metered Licensing.

Bu tür bir lisans almak için gerekli tüm adımları tamamladıktan sonra, lisans dosyası değil, anahtarları alacaksınız. Bu ölçülü anahtar, bu amaç için özel olarak tanıtılan `Metered` sınıfı kullanılarak uygulanabilir.

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

Ölçülü mekanizmanın doğru hesaplamalar için hizmetlerimizle sürekli etkileşimi gerektirdiğinden, ölçülü lisansın doğru kullanımı için istikrarlı bir internet bağlantısına sahip olmanız gerektiğini lütfen unutmayın. Daha fazla bilgi için [“Metered Licensing sss”](https://purchase.aspose.com/faqs/licensing/metered) bölümüne bakın.

{{% /alert %}}



