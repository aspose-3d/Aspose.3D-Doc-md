---
title: Licensing
type: docs
weight: 60
url: /tr/java/licensing/
description: Aspose.3D for Java 'yi değerlendirme için Aspose deposundan kolayca indirebilir/yükleyebilirsiniz. Değerlendirme indirme, satın alınan indirme ile aynıdır. Değerlendirme sürümü, lisansı uygulamak için birkaç kod satırı eklediğinizde lisanslanır.
---
##  **Evaluate Aspose.3D**
You can easily download/install Aspose.3D for Java from [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/) for evaluation. The evaluation download is the same as the purchased download. The evaluation version simply becomes licensed when you add a few lines of code to apply the license.

The değerlendirme sürümü aşağıdakiler hariç tüm özellikleri sağlar:

- Kullanıcılar sadece bir sahne için maksimum 50 3D belgelerini açabilir/içe aktarabilirler.
- Kullanıcılar sadece bir sahne için maksimum 50 3D belgeleri kaydedebilir.
- Users ayrıca işlenmiş görüntülerde ve diğer tüm çıktı dosyalarında bir değerlendirme filigranı görecektir.
- Ach ach düğümü en fazla 5 çocuk düğümüne sahip olamaz.
- Ach ach düğümünün 2'den fazla ekli varlığa sahip olamaz.
- Each geometrisi 2'den fazla ekli vertex elementine sahip olamaz.
- Each düğümü 1'den fazla malzemeye sahip olamaz.

{{% alert color="primary" %}} 

If you're using Aspose.3D without a proper license, there could trigger an **com.aspose.threed.TrialException**Kullanım lisanssız kısıtlamalara ulaştığında, istisnayı şu şekilde kapatabilirsiniz:

* [Tam özellikli bir lisans satın alın](https://purchase.aspose.com/buy).
* Request a 30 days temporary license, please refer to [How to get a Temporary License?](https://purchase.aspose.com/temporary-license) For more information.
.
* Call `com.aspose.threed.TrialException.setSuppressTrialException(true)` before your `open`/`save` methods, the `TrialException` will not be raised during the `open`/`save` call on Scene, but the above restrictions will not be lifted.
* Manually use a `try/catch` block on `Scene.open/save`, this exception is just a notification, ignore it will not affect the scene loading/saving.

{{% /alert %}} 
##  **Applying bir License**
The lisansı, ürün adı, geliştiricilerin sayısı gibi ayrıntıları içeren düz bir metin XML dosyasıdır. The dosyası dijital olarak imzalanır, bu yüzden dosyayı değiştirmeyin; dosyaya ekstra bir hat kırılmasının yanlışlıkla eklenmesi bile geçersiz kılınacaktır. Ybelgelerle herhangi bir işlem yapmadan önce bir lisans ayarlamanız gerekir. Bir cene cene nesnesi oluşturmadan önce bunu you sure emin olun.

Licenses çeşitli konumlardan uygulanabilir:

- Explicit yolu
- Aspose.3D kavanoz dosyasını içeren klasör.
- Aspose.3D jar olarak adlandırılan kavanozda gömülü bir kaynak.

Use the `License.setLicense` method to license the APIs. Often the easiest way to set a license is to put the license file in the same folder as Aspose.3D's JAR and specify just the file name without path.
###  **File Ficense kullanarak File veya Stream Object**
Bu örnekte Aspose.3D, uygulamanızın kavanozlarını içeren klasördeki lisans dosyasını bulmaya çalışacaktır.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingFile.java" >}}

Ibir akımdan bir lisansı nitialize eder.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingStreamObject.java" >}}
###  **Bir Embedded Resource olarak License File ncluding**
Lic dosyasını projenizin `resources` klasöründe kopyalayabilirsiniz. Projenin yeniden inşa edilmesi gerekir. Uygulama içine lic dosyası. Kavanoz dosyası. Bundan sonra aşağıdaki gibi kodu kullanarak lisans uygulayabilirsiniz:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-FileAsEmbeddedResource.java" >}}
###  **Lalidate License**
It, lisansın düzgün ayarlanıp ayarlanmadığını doğrulamak mümkündür. To License sınıfı, lisans düzgün bir şekilde ayarlanmışsa gerçek olacak iscenicensed alanına sahiptir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ValidateLicense.java" >}}
##  **Atered tered etered License**
Aspose.3D allows developers to apply metered key. It is a new licensing mechanism. The new licensing mechanism will be used along with existing licensing method. Those customers who want to be billed based on the usage of the API features can use the metered licensing. For more details, please refer to [Metered Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered) section.

Ölçülü anahtarı uygulamak için yeni bir sınıf `Metered` tanıtıldı. Ölçülü kamu ve özel anahtarın nasıl ayarlanacağını gösteren örnek kod aşağıdadır.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-PublicAndPrivateKeys.java" >}}
##  **Hen hen Lcenicense**
Follow bu basit kurallar:

- The lisansının sadece uygulama alanı başına bir kez ayarlanması gerekiyor.
- Başka bir Aspose kullanmadan önce lisansı ayarlamanız gerekir. 3D sınıfları.
- Calling License. Set. icense birden fazla kez zararlı değildir, ancak sadece işlemci süresini boşa harcar.

If you are developing a class library, you can call License.SetLicense from a static constructor of your class that uses Aspose.3D. The static constructor will execute before an instance of your class is created making sure Aspose.3D license is properly set.
##  **Ou ou can hanhange the iicense File Name**
Lisans dosya adı 'Aspose olmak zorunda değildir. 3D. lic'. İstediğiniz herhangi bir şeye yeniden adlandırabilir ve lisans çağırırken bu ismi kullanabilirsiniz. setlicense.
##  **Exception find annot license filename**
When you purchase and download a license, Aspose website names the license file `Aspose.3D.LIC`. You download the license file using your browser. Some browsers recognize the license file as XML and append an .xml extension to it so the full name of the file on your computer becomes `Aspose.3D.lic.XML`.

When Microsoft Windows, for example, is configured to hide extensions of known file types (unfortunately this is default in most Windows installations), the license file will appear to you as `Aspose.3D.LIC` in Windows Explorer. You are likely to think this is the real file name and call License.SetLicense passing it `Aspose.3D.LIC`, but there is no such file, hence the exception.

Sorunu çözmek için, görünmez kaldırmak için dosyayı yeniden adlandırın. Xml uzantısı. Ayrıca, "uzantılarını gizle" seçeneğini Microsoft Windows olarak devre dışı bırakmanızı öneririz.

##  **Birden fazla api'yi kullanarak Aspose**
If you use multiple Aspose APIs in your application, for example Aspose.3D and Aspose.Cells, here are a few useful tips. 

- Set the License for each Aspose API separately. Even if you have a single license file for all APIs, for example `Aspose.Total.lic`, you still need to call `License.setLicense` separately for each Aspose API you are using in your application.
- Use Fully Qualified License Class Name. Each Aspose API has a License class in its namespace. For example, Aspose.3D has `com.aspose.3d.License` and Aspose.Cells has `com.aspose.cells.License` class. Using the fully qualified class name allows you to avoid any confusion about which license is applied to which product.
