---
title: Declaration
type: docs
weight: 30
url: /tr/net/declaration/
---
{{% alert color="primary" %}} 

Generally, all Aspose .NET components require Full Trust permissions set. The reason is that Aspose for .NET components need to access registry settings, system files other than virtual directory for certain operations like parsing fonts etc. Moreover, Aspose for .NET components (including Aspose.3D for .NET) are based on core .NET system classes that also require Full Trust permissions set in many cases.

{{% /alert %}} 
##  **Kısmi güven/orta güven meydan okuma**
Internet Service Providers hosting multiple applications from different companies mostly enforce a Medium Trust security level. Moreover, sometimes you need to host multiple applications on a shared server, such as in an ISP or other scenarios, you have to use the Medium trust level to constrain the applications. The ASP.NET Medium trust level provides a constrained execution environment that is suitable for isolating multiple applications hosted on ISP servers. In case of .NET 2.0, such a security level may set the following constraints which could affect the ability of Aspose.3D for .NET to perform properly, for example:

- **Kayıt izni mevcut değil**. Bu, hesap tablolarını veya diğer belgeleri oluştururken yüklü yazı tiplerini numaralandırmak için gerekli olan kayıt defterine erişemeyeceğiniz anlamına gelir.
- **Fileiopermisyon sınırlıdır**. Bu, yalnızca uygulamanızın sanal dizin hiyerarşisinde dosyalara erişebileceğiniz anlamına gelir.
##  **Use Aspose.3D for .NET on Medium Trust Permissions Set**
Aspose çalıştırmak için bazı önerileri takip edebilirsiniz. orta güven seviyesinde veya paylaşılan sunucu ortamında 3D for .NET:

- Lisans dosyasını kodunuzda ayarlamak için, lisans dosyasını akışlara aldıktan sonra lisans dosyasını aramanız daha iyidir. lisans (akış) yöntemi.

See the following example that demonstrates on how to use/run Aspose.3D for .NET in Medium Trust mode.

{{< highlight "csharp" >}}

 // Instantiate the License object

Aspose.ThreeD.License lic = new Aspose.ThreeD.License();

// Get the license file into stream

FileStream stream = new FileStream("Aspose._3D.lic", FileMode.Open);

// Set the License stream

lic.SetLicense(stream);

// Close the stream

stream.Close();

//Open the template file

Scene scene = new Scene("test.obj");

// Save the OBJ file

scene.Save("dest.obj", FileFormat.WavefrontOBJ);



{{< /highlight >}}





