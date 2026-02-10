---
title: Licensing
type: docs
weight: 60
url: /es/net/licensing/
description: Descripción general de Licensing Requisitos y limitaciones de la versión de evaluación para procesar formatos de archivo 3D en C#.
---
Descripción general de Licensing Requisitos y limitaciones de la versión de evaluación para procesar formatos de archivo 3D en C#.

##  **Limitaciones de la versión de evaluación**
Una versión de evaluación gratuita de Aspose.3D for .NET se puede descargar de la sección de descargas del sitio web de Aspose en: [Descargar Aspose.3D API](https://www.nuget.org/packages/Aspose.3D).
###  **Limitación**
La versión de evaluación proporciona todas las características excepto las siguientes:

- Los usuarios sólo pueden abrir/importar un máximo de 50 3D documentos a una escena.
- Cada nodo no puede tener más de 5 nodos secundarios.
- Cada nodo no puede tener más de 2 entidades adjuntas.
- Cada geometría no puede tener más de 2 elementos de vértice adjuntos.
- Cada nodo no puede tener más de 1 material.
- Los usuarios solo pueden guardar un máximo de 50 3D documentos en una escena.
- Los usuarios también verán una marca de agua de evaluación en las imágenes renderizadas y en todos los demás archivos de salida.

{{% alert color="primary" %}} 
Si está usando Aspose.3D sin una licencia adecuada, podría activarse un `Aspose.ThreeD.TrialException` cuando el uso alcanzara las restricciones sin licencia, puede desactivar la excepción:

* [Comprar una licencia completa](https://purchase.aspose.com/buy).
* Solicite una licencia temporal de 30 días, consulte [¿Cómo obtener una licencia temporal?](https://purchase.aspose.com/temporary-license) Para obtener más información.
.
* Establezca `Aspose.ThreeD.TrialException.SuppressTrialException` en `true`, el `TrialException` no se elevará durante la llamada `Open/Save` en Scene, pero las restricciones anteriores no se levantarán.
* Utilice manualmente un bloque `try/catch` en `Scene.Open/Save`, esta excepción es solo una notificación, ignorarla no afectará la carga/guardado de la escena.

{{% /alert %}} 

##  **Aplicar licencia mediante archivo u objeto Stream**
La licencia se puede cargar desde [Archivo](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile) o [Objeto stream](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject). Aspose.3D for .NET intentará encontrar la licencia en las siguientes ubicaciones:

1. Camino explícito.
1. La carpeta que contiene Aspose.3D.dll.
1. La carpeta que contiene el ensamblado que llamó Aspose.3D.dll.
1. La carpeta que contiene el ensamblaje de entrada (su. Exe)
1. Recurso incrustado en el ensamblado que llamó Aspose.3D.dll.

La forma más fácil de establecer una licencia es colocar el archivo de licencia en la misma carpeta que el archivo Aspose.3D.dll y especificar el nombre del archivo, sin una ruta, como se muestra en el ejemplo siguiente.

{{% alert color="primary" %}} 

Si está utilizando cualquier otro Aspose for .NET API junto con Aspose.3D for .NET, especifique el espacio de nombres para la licencia como `Aspose.ThreeD.License`.

{{% /alert %}} 
###  **Carga de una licencia del archivo**
La forma más fácil de aplicar una licencia es colocar el archivo de licencia en la misma carpeta que el archivo Aspose.3D.dll y especificar solo el nombre del archivo sin una ruta.

{{% alert color="primary" %}} 

Cuando se llama al método `SetLicense`, el nombre de licencia que se pasa debe ser el del archivo de licencia. Por ejemplo, si cambia el nombre del archivo de licencia a "Aspose.3D.lic.xml" pase ese nombre de archivo al método `threeD.SetLicense(…)`.

{{% /alert %}} 

**Ejemplo:**

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Aspose.ThreeD.License license = new Aspose.ThreeD.License();
license.SetLicense("Aspose._3D.lic");

{{< /highlight >}}
###  ` `**Carga de una licencia de un objeto Stream**
En el ejemplo siguiente se muestra cómo cargar una licencia de una secuencia.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Aspose.ThreeD.License license = new Aspose.ThreeD.License();
FileStream myStream = new FileStream("Aspose._3D.lic", FileMode.Open);
license.SetLicense(myStream);

{{< /highlight >}}
##  **Aplicar licencia usando recurso incrustado**
Una forma de aplicar una licencia es establecerlo [Utilizando un archivo o un objeto de secuencia](). Otra forma de empaquetar la licencia con su aplicación y asegurarse de que no se perderá es incluirlo como un recurso incrustado en uno de los ensamblados que llama a la DLL del componente (incluido en Aspose.3D).

Para incluir el archivo de licencia como un recurso incrustado:

1. En Visual Studio .NET, incluya el archivo de licencia (.lic) en el proyecto seleccionando**Archivo**, Entonces**Agregar elemento existente**Y finalmente**Añadir**.
1. Seleccione el archivo en el Explorador de soluciones.
1. Establecer el**Construir acción**A**Recurso incrustado**En la ventana Propiedades.
1. Para tener acceso a la licencia incrustada en el ensamblado (como recurso incrustado), simplemente agregue el archivo de licencia como recurso incrustado al proyecto y pase el nombre del archivo de licencia al método SetLicense. La clase License busca automáticamente el archivo de licencia en los recursos incrustados. No es necesario llamar a los métodos GetExecutingAssembly y GetManifestResourceStream de la clase System.Reflection.Assembly en el Microsoft .NET Framework.

El siguiente fragmento de código se utiliza para establecer la licencia.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Instantiate the License class
Aspose.ThreeD.License license = new Aspose.ThreeD.License();

// Pass only the name of the license file embedded in the assembly
license.SetLicense("Aspose._3D.lic");

{{< /highlight >}}
##  **Aplicar Licencia Medida**
Aspose.3D for .NET API permite a los desarrolladores aplicar una licencia medida. Es un nuevo sistema de licencias. El nuevo mecanismo de concesión de licencias se utilizará junto con el método de concesión de licencias existente. Aquellos clientes que desean que se les facture según el uso de las características API pueden usar la licencia medida. Para más detalles, consulte la sección [Preguntas frecuentes sobre Licensing medido](https://purchase.aspose.com/faqs/licensing/metered).

Se ha añadido una nueva clase [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered) para aplicar la clave medida. Este ejemplo de código muestra cómo establecer claves públicas y privadas medidas:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize a Metered license class object
Aspose.ThreeD.Metered metered = new Aspose.ThreeD.Metered();
// Set public and private keys
metered.SetMeteredKey("your-public-key", "your-private-key");

{{< /highlight >}}
