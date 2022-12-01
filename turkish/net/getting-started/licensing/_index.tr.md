---
title: Licensing
type: docs
weight: 60
url: /tr/net/licensing/
description: C# yılında 3D dosya formatlarını işlemek için Ricensing equiequiequive Evaluation Version imiimitations verview.
---
C# yılında 3D dosya formatlarını işlemek için Ricensing equiequiequive Evaluation Version imiimitations verview.

## **Edeğerleme Version imiimitations**
A Aspose.3D for .NET ücretsiz değerlendirme sürümü Aspose'in web sitesinin indirme bölümünden indirilebilir:[Ownload load Aspose.3D API](https://www.nuget.org/packages/Aspose.3D).
### **Ltaklit**
The değerlendirme sürümü aşağıdakiler hariç tüm özellikleri sağlar:

- Users sadece 50 3D belgesini Scene 'e açabilir/içe aktarabilir.
- Ach ach düğümü en fazla 5 çocuk düğümüne sahip olamaz.
- Ach ach düğümünün 2'den fazla ekli varlığa sahip olamaz.
- Each geometrisi 2'den fazla ekli vertex elementine sahip olamaz.
- Each düğümü 1'den fazla malzemeye sahip olamaz.
- Users sadece en fazla 50 3D belgesini Scene 'e kaydedebilir.
- Users ayrıca işlenmiş görüntülerde ve diğer tüm çıktı dosyalarında bir değerlendirme filigranı görecektir.

{{% alert color="primary" %}} 
If uygun bir lisans olmadan Aspose.3D kullanıyorsunuz, kullanım lisanssız kısıtlamalara ulaştığında bir `Aspose.ThreeD.TrialException` tetikleyebilir, istisnayı şu şekilde kapatabilirsiniz:

* [Tam özellikli bir lisans](https://purchase.aspose.com/buy).
* Request 30 günlük geçici bir lisans, lütfen [How to get a Temporary License?](https://purchase.aspose.com/temporary-license) Fveya daha fazla bilgi.
.
* Set 'Aspose.ThreeD.TrialException. trueto 'true', 'TrialException' cene 'deki 'Open/Save' çağrısı sırasında kaldırılmayacak, ancak yukarıdaki kısıtlamalar kaldırılmayacaktır.
* Manually 'try cene.Open/Save' üzerinde bir 'try/catch' bloğu kullanın, bu istisna sadece bir bildirim, sahne yükleme/tasarrufu etkilemez görmezden gelir.

{{% /alert %}} 

## **File Ficense kullanarak File veya Stream Object**
The lisansı bir yüklenebilir[Dosya](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile)Veya[Akış nesnesi](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject). Aspose.3D for .NET lisansı aşağıdaki yerlerde bulmaya çalışacaktır:

1. Explicit yolu.
1. To Aspose.3D.dll. içeren klasör.
1. To Aspose.3D.dll.
1. Giriş düzenini içeren The klasörü (senin. Exe).
1. An Aspose.3D.dll. adı verilen montajda gömülü kaynak.

Tbir lisans ayarlamanın en kolay yolu, lisans dosyasını Aspose.3D.dll dosyasıyla aynı klasöre koymaktır ve aşağıdaki örnekte gösterildiği gibi bir yol olmadan dosya adını belirtmektir.

{{% alert color="primary" %}} 

If Aspose.3D 076481 481 ile birlikte herhangi bir Aspose for .NET API kullanarak, lütfen 076. 481 gibi lisans için ad alanını belirtin.

{{% /alert %}} 
### **Foading a License from File**
Tbir lisans uygulamanın en kolay yolu, lisans dosyasını Aspose.3D.dll dosyasıyla aynı klasöre koymaktır ve sadece dosya adını bir yol olmadan belirtmektir.

{{% alert color="primary" %}} 

When `SetLicense` yöntemini aradığınızda, geçtiğiniz lisans adı lisans dosyasından olmalıdır. Fveya örnek, lisans dosya adını "Aspose.3D.lic. xml" olarak değiştirirseniz, bu dosya adını `threeD.SetLicense(…)` yöntemine aktarın.

{{% /alert %}} 

**Ex::**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingFile.cs" >}}
### ` `**Bir treatream Object'den Loading a License**
To aşağıdaki örnek bir akımdan bir lisansın nasıl yükleneceğini gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingStreamObject.cs" >}}
## **Ebedded bedded esource kullanarak Lpply cenicense**
Bir lisans uygulamanın ne yolu ayarlamak[Bir dosya veya akış nesnesi kullanma](). Auygulamanızla lisansın düzgün bir şekilde ambalajlanması ve kaybolmayacağından emin olmak, embedded enin D481 L (Aspose.3D dahil) olarak adlandırılan meclislerden birine gömülü bir kaynak olarak dahil etmektir.

To, lisans dosyasını gömülü bir kaynak olarak içerir:

1. In Visual Studio .NET, lisans (.lic) dosyasını seçerek projeye dahil edin**File**O zaman**Dd dd sting xisting tem tem**Ve sonunda**Add**.
1. Sdosyayı Solution Explorer'de seçin.
1. Set**Build ction ction**Için**Bedded mbedded Resource**Properties penceresinde.
1. To montajda gömülü olan lisansa erişin (gömülü bir kaynak olarak), lisans dosyasını projeye gömülü bir kaynak olarak ekleyin ve lisans dosyasının adını Set. icense yöntemine aktarın. To embedded icense sınıfı, lisans dosyasını gömülü kaynaklarda otomatik olarak bulur. TSystem. Reflection. 07ssembly sınıfı Microsoft .NET Framework.

To aşağıdaki kod parçacığı lisansı ayarlamak için kullanılır.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingEmbeddedResource.cs" >}}
## **Atered tered etered License**
Aspose.3D for .NET API, geliştiricilerin ölçülü lisansı uygulamasına izin verir. It yeni bir lisans mekanizmasıdır. The yeni lisans mekanizması mevcut lisans yöntemi ile birlikte kullanılacaktır. TAPI özelliklerinin kullanımına göre faturalandırılmasını isteyen müşteriler, ölçülü lisanslamayı kullanabilir. Fveya daha fazla detay, lütfen bakın[Tered etered tered icensing FQ Q](https://purchase.aspose.com/faqs/licensing/metered)Bölüm.

Tered yeni sınıf [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered) ölçülü anahtarı uygulamak için eklenmiştir. Tkod örneği, ölçülü kamu ve özel anahtarların nasıl ayarlanacağını gösterir:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-PublicAndPrivateKeys.cs" >}}
