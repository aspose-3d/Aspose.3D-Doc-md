---
title: Declaration
type: docs
weight: 30
url: /es/net/declaration/
---
{{% alert color="primary" %}} 

Por lo general, todos los componentes Aspose .NET requieren permisos de plena confianza establecidos. La razón es que los componentes Aspose for .NET necesitan acceder a la configuración del registro, los archivos del sistema que no sean el directorio virtual para ciertas operaciones como el análisis de fuentes, etc. Además, Aspose for .NET componentes (incluyendo Aspose). 3D for .NET) se basan en las clases principales del sistema .NET que también requieren permisos de plena confianza establecidos en muchos casos.

{{% /alert %}} 
##  **Desafío de confianza parcial/confianza media**
Los proveedores de servicios de Internet que alojan múltiples aplicaciones de diferentes compañías en su mayoría imponen un nivel de seguridad de confianza medio. Además, a veces necesita alojar varias aplicaciones en un servidor compartido, como en un ISP u otros escenarios, debe usar el nivel de confianza Medio para restringir las aplicaciones. El nivel de confianza ASP .NET Medio proporciona un entorno de ejecución restringido que es adecuado para aislar varias aplicaciones alojadas en servidores ISP. En el caso de .NET 2,0, dicho nivel de seguridad puede establecer las siguientes restricciones que podrían afectar la capacidad de Aspose.3D for .NET para funcionar correctamente, por ejemplo:

- **RegistryPermission no está disponible**. Esto significa que no puede acceder al registro, que es necesario para enumerar las fuentes instaladas al representar hojas de cálculo u otros documentos.
- **FileIOPermission está restringido**. Esto significa que solo puede acceder a los archivos de la jerarquía de directorios virtuales de su aplicación.
##  **Utilice Aspose.3D for .NET en el conjunto de permisos de confianza medio**
Puede seguir algunas recomendaciones para ejecutar Aspose.3D for .NET en el nivel de confianza medio o en el entorno de servidor compartido:

- Para establecer el archivo de licencia en su código, es mejor llamar al método License.SetLicense(Stream) en su lugar después de obtener el archivo de licencia en secuencias.

Vea el siguiente ejemplo que demuestra cómo usar/ejecutar Aspose.3D for .NET en el modo de confianza media.

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





