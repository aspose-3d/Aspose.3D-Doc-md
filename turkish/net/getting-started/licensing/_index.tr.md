---
title: Licensing
type: docs
weight: 60
url: /tr/net/licensing/
description: Overview of Licensing Requirements and Evaluation Version Limitations for processing 3D file formats in C#.
---
Overview of Licensing Requirements and Evaluation Version Limitations for processing 3D file formats in C#.

##  **Edeğerleme Version imiimitations**
A free evaluation version of Aspose.3D for .NET can be downloaded from the downloads section of Aspose's website at: [Download Aspose.3D API](https://www.nuget.org/packages/Aspose.3D).
###  **Ltaklit**
The değerlendirme sürümü aşağıdakiler hariç tüm özellikleri sağlar:

- Kullanıcılar sadece 50 3D belgelerini bir sahneyi açabilir/içe aktarabilir.
- Ach ach düğümü en fazla 5 çocuk düğümüne sahip olamaz.
- Ach ach düğümünün 2'den fazla ekli varlığa sahip olamaz.
- Each geometrisi 2'den fazla ekli vertex elementine sahip olamaz.
- Each düğümü 1'den fazla malzemeye sahip olamaz.
- Kullanıcılar sadece bir sahne için en fazla 50 3D belgesini kaydedebilir.
- Users ayrıca işlenmiş görüntülerde ve diğer tüm çıktı dosyalarında bir değerlendirme filigranı görecektir.

{{% alert color="primary" %}} 
If you're using Aspose.3D without a proper license, there could trigger an `Aspose.ThreeD.TrialException` when the usage reached the unlicensed restrictions, you can turn the exception off by:

* [Tam özellikli bir lisans satın alın](https://purchase.aspose.com/buy).
* Request a 30 days temporary license, please refer to [How to get a Temporary License?](https://purchase.aspose.com/temporary-license) For more information.
.
* Set `Aspose.ThreeD.TrialException.SuppressTrialException` to `true`, the `TrialException` will not be raised during the `Open/Save` call on Scene, but the above restrictions will not be lifted.
* Manually use a `try/catch` block on `Scene.Open/Save`, this exception is just a notification, ignore it will not affect the scene loading/saving.

{{% /alert %}} 

##  **File Ficense kullanarak File veya Stream Object**
The license can be loaded from a [file](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile) or [stream object](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject). Aspose.3D for .NET will try to find the license in the following locations:

1. Explicit yolu.
1. Aspose.3D.dll içeren klasör.
1. Aspose.3D.dll adı verilen montajı içeren klasör.
1. Giriş düzenini içeren The klasörü (senin. Exe).
1. An embedded resource in the assembly that called Aspose.3D.dll.

Bir lisans ayarlamanın en kolay yolu, lisans dosyasını Aspose ile aynı klasöre koymaktır. 3D.dll dosyası ve aşağıdaki örnekte gösterildiği gibi dosya adını belirtin.

{{% alert color="primary" %}} 

If you are using any other Aspose for .NET API along with Aspose.3D for .NET, please specify the namespace for the license like `Aspose.ThreeD.License`.

{{% /alert %}} 
###  **Foading a License from File**
Bir lisans uygulamanın en kolay yolu, lisans dosyasını Aspose ile aynı klasöre koymaktır. 3D.dll dosyası ve sadece dosya adını bir yol olmadan belirtin.

{{% alert color="primary" %}} 

When you call the `SetLicense` method, the license name that you pass should be that of the license file. For example, if you change the license file name to "Aspose.3D.lic.xml" pass that filename to `threeD.SetLicense(…)` method.

{{% /alert %}} 

**Ex::**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingFile.cs" >}}
###  ` `**Bir treatream Object'den Loading a License**
To aşağıdaki örnek bir akımdan bir lisansın nasıl yükleneceğini gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingStreamObject.cs" >}}
##  **Ebedded bedded esource kullanarak Lpply cenicense**
One way of applying a license is to set it [using a file or stream object](). Another neat way of packaging the license with your application and making sure it will not be lost is to include it as an embedded resource into one of the assemblies that calls the component's DLL (included in Aspose.3D).

To, lisans dosyasını gömülü bir kaynak olarak içerir:

1. Görsel stüdyoda .NET, seçerek projeye lisans (.lic) dosyasını ekleyin**File**O zaman**Dd dd sting xisting tem tem**Ve sonunda**Add**.
1. Sdosyayı Solution Explorer'de seçin.
1. Set**Build ction ction**Için**Bedded mbedded Resource**Properties penceresinde.
1. Montajda gömülü olan lisansa (gömülü bir kaynak olarak) erişmek için, lisans dosyasını projeye gömülü bir kaynak olarak ekleyin ve lisans dosyasının adını setlicense yöntemine iletin. Lisans sınıfı, lisans dosyasını gömülü kaynaklarda otomatik olarak bulur. Sistemin getexecutingassembly ve getmanifestresourcestream yöntemlerini aramaya gerek yoktur. yansıma. montaj sınıfı Microsoft .NET çerçevesinde.

To aşağıdaki kod parçacığı lisansı ayarlamak için kullanılır.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingEmbeddedResource.cs" >}}
##  **Atered tered etered License**
Aspose.3D for .NET API allows developers to apply metered license. It is a new licensing mechanism. The new licensing mechanism will be used along with existing licensing method. Those customers who want to be billed based on the usage of the API features can use the metered licensing. For more details, please refer to [Metered Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered) section.

A new class [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered) has been added to apply metered key. This code example demonstrates how to set metered public and private keys:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-PublicAndPrivateKeys.cs" >}}
