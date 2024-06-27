---
title: Declaration
type: docs
weight: 30
url: /de/net/declaration/
---
{{% alert color="primary" %}} 

Im Allgemeinen benötigen alle Aspose .NET-Komponenten den Satz Full Trust-Berechtigungen. Der Grund dafür ist, dass Aspose for .NET-Komponenten für bestimmte Vorgänge wie das Parsen von Schriftarten usw. auf Registrierung seins tel lungen, andere System dateien als das virtuelle Verzeichnis zugreifen müssen. Darüber hinaus Aspose for .NET Komponenten (einschl ießlich Aspose.3D for .NET) basieren auf den Kerns ystem klassen .NET, für die in vielen Fällen auch Full Trust-Berechtigungen festgelegt werden müssen.

{{% /alert %}} 
##  **Partielle Vertrauens-/mittlere Vertrauens herausforderung**
Internet dienst anbieter, die mehrere Anwendungen verschiedener Unternehmen hosten, erzwingen haupt sächlich eine Sicherheits stufe von Medium Trust. Darüber hinaus müssen Sie manchmal mehrere Anwendungen auf einem freigegebenen Server hosten, z. B. in einem ISP oder in anderen Szenarien. Sie müssen die mittlere Vertrauens ebene verwenden, um die Anwendungen einzu schränken. Die ASP .NET Medium-Vertrauens ebene bietet eine einges chränkte Ausführungs umgebung, die zum Isolieren mehrerer auf ISP-Servern gehosteter Anwendungen geeignet ist. Im Falle von .NET 2.0 kann eine solche Sicherheits stufe die folgenden Einschränkungen festlegen, die sich beispiels weise auf die Fähigkeit von Aspose auswirken können. 3D for .NET, ordnungs gemäß zu arbeiten:

- **Registrierung Berechtigung ist nicht verfügbar**. Dies bedeutet, dass Sie nicht auf die Registrierung zugreifen können, die zum Aufzählen installierter Schriftarten beim Rendern von Tabellen kalkulationen oder anderen Dokumenten erforderlich ist.
- **File IO Permission ist einges chränkt**. Dies bedeutet, dass Sie nur auf Dateien in der virtuellen Verzeichnis hierarchie Ihrer Anwendung zugreifen können.
##  **Verwenden Sie Aspose.3D for .NET für mittlere Vertrauens berechtigungen**
Sie können einige Empfehlungen befolgen, um Aspose.3D for .NET auf mittlerer Trust-Ebene oder einer gemeinsam genutzten Server-Umgebung auszuführen:

- Um die Lizenz datei in Ihrem Code festzulegen, sollten Sie stattdessen die License.SetLicense(Stream)-Methode aufrufen, nachdem Sie die Lizenz datei in Streams erhalten haben.

Sehen Sie sich das folgende Beispiel an, das zeigt, wie Sie Aspose.3D for .NET im Medium Trust-Modus verwenden/ausführen.

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





