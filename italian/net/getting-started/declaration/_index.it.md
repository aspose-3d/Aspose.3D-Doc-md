---
title: Declaration
type: docs
weight: 30
url: /it/net/declaration/
---
{{% alert color="primary" %}} 

In genere, tutti i componenti Aspose .NET richiedono le autorizzazioni Full Trust impostate. Il motivo è che i componenti Aspose for .NET devono accedere alle impostazioni del registro, ai file di sistema diversi dalla directory virtuale per determinate operazioni come analizzare i caratteri ecc. Inoltre, Aspose for .NET componenti (inclusi Aspose.3D for .NET) si basano su classi di sistema di base .NET che in molti casi richiedono anche autorizzazioni Full Trust impostate.

{{% /alert %}} 
##  **Fiducia parziale/media fiducia sfida**
I provider di servizi Internet che ospitano più applicazioni di diverse società impongono principalmente un livello di sicurezza Medium Trust. Inoltre, a volte è necessario ospitare più applicazioni su un server condiviso, ad esempio in un ISP o in altri scenari, è necessario utilizzare il livello di fiducia medio per limitare le applicazioni. Il livello di fiducia medio ASP .NET fornisce un ambiente di esecuzione limitato adatto per isolare più applicazioni ospitate su server ISP. Nel caso di .NET 2.0, tale livello di sicurezza può impostare i seguenti vincoli che potrebbero influire sulla capacità di Aspose.3D for .NET per eseguire correttamente, ad esempio:

- **RegistryPermission non è disponibile**. Ciò significa che non è possibile accedere al registro, che è necessario per enumerare i caratteri installati durante il rendering di fogli di calcolo o altri documenti.
- **FileIOPermission è limitato**. Ciò significa che puoi accedere solo ai file nella gerarchia delle directory virtuali dell'applicazione.
##  **Usa Aspose.3D for .NET sul set di permessi di trust medio**
Puoi seguire alcuni consigli per eseguire Aspose.3D for .NET a livello di media fiducia o ambiente server condiviso:

- Per impostare il file di licenza nel codice, è meglio chiamare il metodo License.SetLicense(Stream) invece dopo aver ottenuto il file di licenza in stream.

Vedere il seguente esempio che mostra come utilizzare/eseguire Aspose.3D for .NET in modalità Media Trust.

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





