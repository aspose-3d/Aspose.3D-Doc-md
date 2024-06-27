---
title: Declaration
type: docs
weight: 30
url: /sv/net/declaration/
---
{{% alert color="primary" %}} 

Generellt kräver alla Aspose .NET-komponenter fullständiga förtroendebehörigheter. Anledningen är att Aspose for .NET komponenter måste komma åt registerinställningar, systemfiler andra än virtuell katalog för vissa åtgärder som att tolka teckensnitt etc. Dessutom, Aspose for .NET komponenter (inklusive Aspose. 3D for .NET) baseras på kärnklass i .NET som också kräver fullständig förtroendebehörighet som ställs in i många fall.

{{% /alert %}} 
##  **Partiellt förtroende / Medel förtroendeutmaning**
Internettjänsteleverantörer som värd flera applikationer från olika företag upprätthåller oftast en säkerhetsnivå för Medium Trust. Dessutom behöver du ibland vara värd för flera program på en delad server, t.ex. i en ISP eller andra scenarier, du måste använda den medelstora förtroendenivån för att begränsa applikationerna. ASP.NET Medelförtroendenivån tillhandahåller en begränsad körningsmiljö som är lämplig för att isolera flera program som är värd på. ISP-servrar. Vid .NET 2.0 kan en sådan säkerhetsnivå ställa följande begränsningar som kan påverka förmågan för Aspose. 3D for .NET att utföra korrekt, till exempel:

- **RegistryPermission är inte tillgängligName**. Detta innebär att du inte kan komma åt registret, som krävs för att räkna upp installerade teckensnitt när kalkylblad eller andra dokument återges.
- **FileIOPermission är begränsad**. Detta innebär att du bara kan komma åt filer i programmets virtuella kataloghierarki.
##  **Använd Aspose.3D for .NET på medelstora förtroendebehörighet**
Du kan följa rekommendationer för att köra Aspose.3D for .NET på medelstillförtroendenivå eller delad servermiljö:

- För att ställa in licensfil i koden är det bättre att du ringer Licensen. SetLicense (Stream) metod istället efter att ha fått licensfilen i strömmar.

Se följande exempel som visar hur man använder eller kör Aspose.3D for .NET i medelstillförtroende.

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





