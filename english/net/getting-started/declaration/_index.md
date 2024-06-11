---
title: Declaration
type: docs
weight: 30
url: /net/declaration/
---

{{% alert color="primary" %}} 

Generally, all Aspose .NET components require Full Trust permissions set. The reason is that Aspose for .NET components need to access registry settings, system files other than virtual directory for certain operations like parsing fonts etc. Moreover, Aspose for .NET components (including Aspose.3D for .NET) are based on core .NET system classes that also require Full Trust permissions set in many cases.

{{% /alert %}} 
## **Partial Trust / Medium Trust Challenge**
Internet Service Providers hosting multiple applications from different companies mostly enforce a Medium Trust security level. Moreover, sometimes you need to host multiple applications on a shared server, such as in an ISP or other scenarios, you have to use the Medium trust level to constrain the applications. The ASP.NET Medium trust level provides a constrained execution environment that is suitable for isolating multiple applications hosted on ISP servers. In case of .NET 2.0, such a security level may set the following constraints which could affect the ability of Aspose.3D for .NET to perform properly, for example:

- **RegistryPermission is not available**. This means you cannot access the registry, which is required to enumerate installed fonts when rendering spreadsheets or other documents.
- **FileIOPermission is restricted**. This means you can only access files in your application's virtual directory hierarchy.
## **Use Aspose.3D for .NET on Medium Trust Permissions Set**
You may follow some recommendations to run Aspose.3D for .NET on Medium Trust level or shared server environment:

- To set license file in your code, it's better you should call the License.SetLicense(Stream) method instead after obtaining the license file into streams.

See the following example that demonstrates on how to use/run Aspose.3D for .NET in Medium Trust mode.

{{< highlight csharp >}}

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





