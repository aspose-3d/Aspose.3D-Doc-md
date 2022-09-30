---
title: Licencias
type: docs
weight: 60
url: /es/net/licensing/
description: Descripción general de los requisitos de licencia y las limitaciones de versión de evaluación para procesar formatos de archivo 3D en C#.
---
Descripción general de los requisitos de licencia y las limitaciones de versión de evaluación para procesar formatos de archivo 3D en C#.

## **Limitaciones de la versión de evaluación**
Se puede descargar una versión de evaluación gratuita de Aspose.3D for .NET desde la sección de descargas del sitio web del Aspose en:[Descargar Aspose.3D API](https://www.nuget.org/packages/Aspose.3D).
### **Limitación**
La versión de evaluación proporciona todas las características excepto las siguientes:

- Los usuarios solo pueden abrir/importar un máximo de 50 documentos 3D a una escena.
- Cada nodo no puede tener más de 5 nodos secundarios.
- Cada nodo no puede tener más de 2 entidades adjuntas.
- Cada geometría no puede tener más de 2 elementos de vértice adjuntos.
- Cada nodo no puede tener más de 1 material.
- Los usuarios solo pueden guardar un máximo de 50 documentos 3D en una escena.
- Los usuarios también verán una marca de agua de evaluación en las imágenes renderizadas y en todos los demás archivos de salida.

{{% alert color="primary" %}} 
Si está utilizando Aspose.3D sin una licencia adecuada, podría desencadenar un `Aspose.ThreeD.TrialException` cuando el uso alcanzó las restricciones sin licencia, puede desactivar la excepción:

* [Compre una licencia completa](https://purchase.aspose.com/buy).
* Solicite una licencia temporal de 30 días, consulte [¿Cómo obtener una licencia temporal?](https://purchase.aspose.com/temporary-license) Para obtener más información.
.
* Set 'Aspose.ThreeD. TrialExcepción. SupressidosTrialException' a 'verdad', la 'Excepción Trial' no se planteará durante la llamada 'Abrir/Salvar' en Scene, pero las restricciones anteriores no se levantarán.
* Utilice manualmente un bloque 'probar/catch' en 'Escena. Abrir/Guardar', esta excepción es solo una notificación, ignore que no afectará a la carga/guardado de la escena.

{{% /alert %}} 

## **Aplicar licencia mediante archivo u objeto Stream**
La licencia se puede cargar desde un[Archivo](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile)O[Objeto stream](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject)... Aspose.3D for .NET intentará encontrar la licencia en las siguientes ubicaciones:

1. Camino explícito.
1. La carpeta que contiene Aspose.3D.dll.
1. La carpeta que contiene el ensamblaje que llamó Aspose.3D.dll.
1. La carpeta que contiene el ensamblaje de entrada (su. Exe)
1. Un recurso incrustado en la asamblea que llamó Aspose.3D.dll.

La forma más fácil de establecer una licencia es colocar el archivo de licencia en la misma carpeta que el archivo Aspose.3D.dll y especificar el nombre del archivo, sin una ruta, como se muestra en el ejemplo siguiente.

{{% alert color="primary" %}} 

Si está utilizando cualquier otro Aspose for .NET API junto con Aspose.3D for .NET, especifique el espacio de nombres para la licencia como `Aspose.ThreeD.License`.

{{% /alert %}} 
### **Carga de una licencia del archivo**
La forma más fácil de aplicar una licencia es colocar el archivo de licencia en la misma carpeta que el archivo Aspose.3D.dll y especificar solo el nombre del archivo sin una ruta.

{{% alert color="primary" %}} 

Cuando llame al método `SetLicense`, el nombre de licencia que apruebe debe ser el del archivo de licencia. Por ejemplo, si cambia el nombre del archivo de licencia a "Aspose.3D.lic. xml", pase ese nombre de archivo al método `threeD.SetLicense(…)`.

{{% /alert %}} 

**Ejemplo:**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingFile.cs" >}}
### ` `**Carga de una licencia de un objeto Stream**
En el ejemplo siguiente se muestra cómo cargar una licencia de una secuencia.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingStreamObject.cs" >}}
## **Aplicar licencia usando recurso incrustado**
Una forma de aplicar una licencia es fijarla[Utilizando un archivo o un objeto de secuencia]()... Otra forma ordenada de empaquetar la licencia con su aplicación y asegurarse de que no se pierda es incluirlo como un recurso incrustado en uno de los ensamblajes que llama al DLL del componente (incluido en Aspose.3D).

Para incluir el archivo de licencia como un recurso incrustado:

1. En Visual Studio .NET, incluya el archivo de licencia (.lic) en el proyecto seleccionando**Archivo**, Entonces**Agregar elemento existente**Y finalmente**Añadir**.
1. Seleccione el archivo en el Explorador de soluciones.
1. Establecer el**Construir acción**A**Recurso incrustado**En la ventana Propiedades.
1. Para acceder a la licencia incrustada en el ensamblado (como un recurso incrustado), simplemente agregue el archivo de licencia como un recurso incrustado al proyecto y pase el nombre del archivo de licencia al método SetLicense. La clase License busca automáticamente el archivo de licencia en los recursos incrustados. No es necesario llamar a los métodos GetExecutingAssembly y GetManifestResourceStream de la clase System.Reflection.Assembly en Microsoft .NET Framework.

El siguiente fragmento de código se utiliza para establecer la licencia.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingEmbeddedResource.cs" >}}
## **Aplicar Licencia Medida**
Aspose.3D for .NET API permite a los desarrolladores aplicar una licencia medida. Es un nuevo mecanismo de concesión de licencias. El nuevo mecanismo de concesión de licencias se utilizará junto con el método de concesión de licencias existente. Aquellos clientes que quieran ser facturados según el uso de las funciones API pueden usar la licencia medida. Para obtener más detalles, consulte[Preguntas frecuentes sobre licencias métricas](https://purchase.aspose.com/faqs/licensing/metered)Sección.

Se ha agregado una nueva clase [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered) para aplicar la clave medida. Este ejemplo de código muestra cómo establecer claves públicas y privadas con medida:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-PublicAndPrivateKeys.cs" >}}
