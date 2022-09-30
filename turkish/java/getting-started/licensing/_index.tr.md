---
title: Licensing
type: docs
weight: 60
url: /tr/java/licensing/
description: You Aspose.3D for Java Aspose Repository değerlendirme için kolayca indirebilir/kurabilir. The değerlendirme indirme, satın alınan indirme ile aynıdır. To değerlendirme sürümü, lisansı uygulamak için birkaç kod satırı eklediğinizde lisanslanır.
---
## **E07ate Aspose.3D**
07ou Aspose.3D for Java 'i kolayca indirebilir/kurabilir[Aspose Repository](http://repository.aspose.com/repo/com/aspose/aspose-3d/)Değerlendirme için. The değerlendirme indirme, satın alınan indirme ile aynıdır. To değerlendirme sürümü, lisansı uygulamak için birkaç kod satırı eklediğinizde lisanslanır.

The değerlendirme sürümü aşağıdakiler hariç tüm özellikleri sağlar:

- Users sadece bir cene cene için maksimum 50 3D belgesini açabilir/içe aktarabilir.
- Users sadece maksimum 50 3D belgesini Scene 'e kaydedebilir.
- Users ayrıca işlenmiş görüntülerde ve diğer tüm çıktı dosyalarında bir değerlendirme filigranı görecektir.
- Ach ach düğümü en fazla 5 çocuk düğümüne sahip olamaz.
- Ach ach düğümünün 2'den fazla ekli varlığa sahip olamaz.
- Each geometrisi 2'den fazla ekli vertex elementine sahip olamaz.
- Each düğümü 1'den fazla malzemeye sahip olamaz.

{{% alert color="primary" %}} 

If uygun bir lisans olmadan Aspose.3D kullanıyorsunuz, bir tetikleyebilir**com.aspose.threed.TrialException**Kullanım lisanssız kısıtlamalara ulaştığında, istisnayı şu şekilde kapatabilirsiniz:

* [Tam özellikli bir lisans](https://purchase.aspose.com/buy).
* Request 30 günlük geçici bir lisans, lütfen [How to get a Temporary License?](https://purchase.aspose.com/temporary-license) Fveya daha fazla bilgi.
.
* Call 'com.aspose.threed.TrialException. '( doğru) ''açık'/'save' yöntemlerinden önce, 'TrialException' 'açık'/'save' çağrısı sırasında kaldırılmayacak, ancak yukarıdaki kısıtlamalar kaldırılmayacaktır.
* Manually 'try cene.open/save' üzerinde bir 'try/catch' bloğu kullanın, bu istisna sadece bir bildirim, sahne yükleme/tasarrufu etkilemez görmezden gelir.

{{% /alert %}} 
## **Applying bir License**
The lisansı, ürün adı, geliştiricilerin sayısı gibi ayrıntıları içeren düz bir metin XML dosyasıdır. The dosyası dijital olarak imzalanır, bu yüzden dosyayı değiştirmeyin; dosyaya ekstra bir hat kırılmasının yanlışlıkla eklenmesi bile geçersiz kılınacaktır. Ybelgelerle herhangi bir işlem yapmadan önce bir lisans ayarlamanız gerekir. Bir cene cene nesnesi oluşturmadan önce bunu you sure emin olun.

Licenses çeşitli konumlardan uygulanabilir:

- Explicit yolu
- To Aspose.3D'in JAR dosyasını içeren klasör.
- 07n Aspose.3D Jcalled called denilen JAiçinde gömülü kaynak.

AAIs lisansı için `License.setLicense` yöntemini kullanın. Often bir lisans ayarlamanın en kolay yolu, lisans dosyasını Aspose.3D'in JAR ile aynı klasöre koymaktır ve sadece dosya adını yolsuz olarak belirtmektir.
### **File Ficense kullanarak File veya Stream Object**
In bu örnek Aspose.3D, lisans dosyasını uygulamanızın JARs içeren klasörde bulmaya çalışacaktır.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingFile.java" >}}

Ibir akımdan bir lisansı nitialize eder.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingStreamObject.java" >}}
### **Bir Embedded Resource olarak License File ncluding**
You, projenizin `resources` klasöründe LIC dosyasını kopyalayabilir. Proje inşa etmek gerekir. Uygulama içine lic dosyası. Kavanoz dosyası. Aşağıdaki gibi kodu kullanarak lisans uygulayabileceğiniz fter fter:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-FileAsEmbeddedResource.java" >}}
### **Lalidate License**
It, lisansın düzgün ayarlanıp ayarlanmadığını doğrulamak mümkündür. To License sınıfı, lisans düzgün bir şekilde ayarlanmışsa gerçek olacak iscenicensed alanına sahiptir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ValidateLicense.java" >}}
## **Atered tered etered License**
Aspose.3D, geliştiricilerin ölçülü anahtarı uygulamasına izin verir. It yeni bir lisans mekanizmasıdır. The yeni lisans mekanizması mevcut lisans yöntemi ile birlikte kullanılacaktır. 07API özelliklerinin kullanımına göre faturalandırılmasını isteyen hortum müşterileri, ölçülü lisanslamayı kullanabilir. Fveya daha fazla detay, lütfen bakın[Tered etered tered icensing FQ Q](https://purchase.aspose.com/faqs/licensing/metered)Bölüm.

Tered yeni sınıf `Metered` ölçülü anahtarı uygulamak için tanıtıldı. Fol., ölçülü kamu ve özel anahtarın nasıl ayarlanacağını gösteren örnek koddur.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-PublicAndPrivateKeys.java" >}}
## **Hen hen Lcenicense**
Follow bu basit kurallar:

- The lisansının sadece uygulama alanı başına bir kez ayarlanması gerekiyor.
- You başka Aspose.3D sınıfları kullanmadan önce lisansı ayarlamanız gerekir.
- Calling License. Set. icense birden fazla kez zararlı değildir, ancak sadece işlemci süresini boşa harcar.

If bir sınıf kütüphanesi geliştiriyorsunuz, License. SetLicense'yi Aspose.3D kullanan sınıfınızın statik bir yapıcısından arayabilirsiniz. To statik oluşturucu, sınıfınızın bir örneği oluşturulmadan önce Aspose.3D lisansının uygun şekilde ayarlandığından emin olacaktır.
## **Ou ou can hanhange the iicense File Name**
To lisans dosyası adı 'Aspose.3D.LIC' olmak zorunda değildir. You, beğendiğiniz herhangi bir şeye yeniden adlandırabilir ve License. Set. icense.
## **Exception find annot license filename**
Bir lisans satın alıp indirirseniz, Aspose web sitesi lisans dosyasını `Aspose.3D.LIC` olarak adlandırır. You tarayıcınızı kullanarak lisans dosyasını indirin. Some tarayıcıları lisans dosyasını XML olarak tanımlar ve bir ekleyin. Xml uzantısı, böylece bilgisayarınızdaki dosyanın tam adı `Aspose.3D.lic.XML` olur.

Örneğin, hen hen Microsoft Windows, bilinen dosya türlerinin uzantılarını gizlemek için yapılandırılmıştır (maalesef bu çoğu Windows kurulumunda varsayılan olarak saptanmıştır), lisans dosyası `Aspose.3D.LIC` yılında 076481 481 Explorer olarak size görünecektir. You bunun gerçek dosya adı olduğunu ve License.SetLicense 076. 481 geçiyor, ancak böyle bir dosya yok, dolayısıyla istisna.

Sorunu çözmek için In siparişi, görünmez kaldırmak için dosyayı yeniden adlandırın. Xml uzantısı. We ayrıca Microsoft Windows yılında "uzantılarını gizle" seçeneğini devre dışı bırakmanızı da tavsiye eder.

## **07sing ultiultiple APIs Aspose**
If uygulamanızda çoklu Aspose APIs kullanıyorsunuz, örneğin Aspose.3D ve Aspose.Cells, burada birkaç yararlı ipucu var.

- Her Aspose API için ayrı ayrı License. Even tüm APIs için tek bir lisans dosyanız varsa, örneğin `Aspose.Total.lic`, uygulamanızda kullandığınız her 076481 481 076481 481 için ayrı ayrı `License.setLicense` numaralı telefonu aramanız gerekir.
- Use Fully fied ualified License lass. ame. Ach ach Aspose API, ad alanında License sınıfına sahiptir. Fveya örnek, Aspose.3D `com.aspose.3d.License` ve 076481 481 076. 481 sınıfına sahiptir. Tam nitelikli sınıf adını söylemek, hangi lisansın hangi ürüne uygulandığına dair herhangi bir karışıklıktan kaçınmanızı sağlar.
