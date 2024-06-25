---
title: Licensing
description: Aspose.3D for Python via .NET proporciona diferentes planes de compra u ofrece una prueba gratuita y una licencia temporal de 30 días para evaluación utilizando Licensing y las políticas de suscripción
type: docs
weight: 80
url: /es/python-net/licensing/
---
A veces, para estudiar mejor el sistema, desea sumergirse en el código lo más rápido posible. Para hacer esto más fácil, Aspose.3D proporciona diferentes planes de compra u ofrece una prueba gratuita y una licencia temporal de 30 días para evaluación.

{{% alert color="primary" %}}

Tenga en cuenta que hay una serie de políticas y prácticas generales que lo guían sobre cómo evaluar, licenciar adecuadamente y comprar nuestros productos. Puedes encontrarlos en la sección ["Políticas de compra y preguntas frecuentes"](https://purchase.aspose.com/policies).

{{% /alert %}}

##  **Evaluar Aspose.3D**
Puede descargar fácilmente Aspose.3D para su evaluación. El paquete de evaluación es el mismo que el paquete comprado. La versión de evaluación simplemente adquiere licencia después de agregar algunas líneas de código para aplicar la licencia.

##  **Limitación de versión de evaluación**
La versión de evaluación proporciona todas las características excepto las siguientes:

- Los usuarios sólo pueden abrir/importar un máximo de 50 3D documentos a una escena.
- Cada nodo no puede tener más de 5 nodos secundarios.
- Cada nodo no puede tener más de 2 entidades adjuntas.
- Cada geometría no puede tener más de 2 elementos de vértice adjuntos.
- Cada nodo no puede tener más de 1 material.
- Los usuarios solo pueden guardar un máximo de 50 3D documentos en una escena.
- Los usuarios también verán una marca de agua de evaluación en las imágenes renderizadas y en todos los demás archivos de salida.

{{% alert color="primary" %}} 
Si está usando Aspose.3D sin una licencia adecuada, podría activarse un `aspose.threed.TrialException` cuando el uso alcanzara las restricciones sin licencia, puede desactivar la excepción:

* [Comprar una licencia completa](https://purchase.aspose.com/buy).
* Solicite una licencia temporal de 30 días, consulte [¿Cómo obtener una licencia temporal?](https://purchase.aspose.com/temporary-license) Para obtener más información.
* Utilice manualmente un bloque `try/except` en `Scene.open/save`, esta excepción es solo una notificación, ignorarla no afectará la carga/guardado de la escena.

{{% /alert %}} 


##  **Acerca de la licencia**
Puede descargar fácilmente una versión de evaluación de Aspose.3D for Python via .NET desde su [Página de descarga](https://pypi.org/project/aspose.3d/). La versión de evaluación proporciona absolutamente**Las mismas capacidades**Como la versión con licencia de Aspose.3D. Además, la versión de evaluación simplemente se licencia después de comprar una licencia y agregar un par de líneas de código para aplicar la licencia.

La licencia es un archivo XML de texto sin formato que contiene detalles como el nombre del producto, el número de desarrolladores a los que tiene licencia, la fecha de vencimiento de la suscripción, etc. El archivo está firmado digitalmente, así que no modifique el archivo. Incluso una adición inadvertida de un salto de línea adicional al contenido del archivo lo invalidará.

Para evitar las limitaciones asociadas con la versión de evaluación, debe establecer una licencia antes de usar**Aspose.3D**... Sólo debe establecer una licencia una vez por solicitud o proceso.

## Licencia comprada

Después de la compra, debe aplicar el archivo de licencia o la transmisión. Esta sección describe las opciones de cómo se puede hacer esto y también comenta algunas preguntas comunes.

{{% alert color="primary" %}}

Necesita establecer la licencia:
* Sólo una vez por dominio de aplicación
* Antes de usar cualquier otra clase Aspose.3D

{{% /alert %}}

{{% alert color="primary" %}}

Puede encontrar información sobre precios en la página [“Información de precios”](https://purchase.aspose.com/pricing/3d/family).

{{% /alert %}}

###  **Establecer una licencia en Aspose.3D for Python via .NET**

Las licencias se pueden aplicar desde varios lugares:

* Trayectoria explícita
* La carpeta que contiene el script de Python que llama a Aspose.3D for Python via .NET
* Corriente
* Como una licencia medida-un nuevo mecanismo de concesión de licencias

{{% alert color="primary" %}}

Utilice el método `set_license` para obtener la licencia de un componente.

Llamar a `set_license` varias veces no es dañino, solo desperdicia el tiempo del procesador.

{{% /alert %}}

En las siguientes secciones, describiremos los dos métodos comunes utilizados para establecer la licencia.

####  **Aplicación de una licencia mediante un archivo**
El método más fácil de establecer una licencia requiere que coloque el archivo de licencia en la misma carpeta que contiene el script de python que llama a Aspose.3D para Python y especifique solo el nombre del archivo sin su ruta.

Este fragmento de código se utiliza para establecer un archivo de licencia:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license("Aspose.3D.lic")
```

Al llamar al método `set_license`, el nombre de la licencia debe ser el mismo que el del archivo de licencia. Por ejemplo, puede cambiar el nombre del archivo de licencia a "Aspose.3D.lic.xml". Luego, en su código, debe pasar el nuevo nombre de licencia (Aspose.3D.lic.xml) al método SetLicense.

####  **Aplicación de una licencia de un Stream**
Puede cargar una licencia desde una secuencia.

Este fragmento de código se utiliza para aplicar una licencia de una secuencia:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license(stream)
```

#### Aplicar Licencia Medida

Aspose.3D permite a los desarrolladores aplicar una clave medida. Se trata de un nuevo sistema de licencias.

El nuevo mecanismo de concesión de licencias se utilizará junto con el método de concesión de licencias existente. Los clientes que deseen que se les facture en función del uso de las funciones API pueden usar Metered Licensing.

Después de completar todos los pasos necesarios para obtener este tipo de licencia, recibirá las claves, no el archivo de licencia. Esta clave medida se puede aplicar usando la clase `Metered` especialmente introducida para este propósito.

El ejemplo de código siguiente muestra cómo establecer claves públicas y privadas con medida:

```py
import aspose.threed as a3d

# Create an instance of CAD Metered class
metered = a3d.Metered()

# Access the set_metered_key property and pass public and private keys as parameters
metered.set_metered_key("*****", "*****")

# Get metered data amount before calling API
amountbefore = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed Before: " + str(amountbefore))

# Load the scene from disk.
scene = a3d.Scene.from_file("3D Model.fbx")
# Save as pdf
scene.save("out_pdf.pdf", a3d.FileFormat.PDF)

# Get metered data amount After calling API
amountafter = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed After: " + str(amountafter))
```

{{% alert color="primary" %}}

Tenga en cuenta que debe tener una conexión estable a Internet para el correcto uso de la licencia Medida, ya que el mecanismo Medida requiere la interacción constante con nuestros servicios para los cálculos correctos. Para más detalles, consulte la sección [“Preguntas frecuentes sobre Licensing medido”](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}}



