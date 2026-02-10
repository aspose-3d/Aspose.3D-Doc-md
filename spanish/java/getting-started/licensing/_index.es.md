---
title: Licensing
type: docs
weight: 60
url: /es/java/licensing/
description: Puede descargar/instalar fácilmente Aspose.3D for Java desde el repositorio Aspose para su evaluación. La descarga de evaluación es la misma que la descarga comprada. La versión de evaluación simplemente se licencia cuando se agregan unas pocas líneas de código para aplicar la licencia.
---
##  **Evaluar Aspose.3D**
Puede descargar/instalar fácilmente Aspose.3D for Java desde [Repositorio Aspose](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/) para su evaluación. La descarga de evaluación es la misma que la descarga comprada. La versión de evaluación simplemente se licencia cuando se agregan unas pocas líneas de código para aplicar la licencia.

La versión de evaluación proporciona todas las características excepto las siguientes:

- Los usuarios solo pueden abrir/importar un máximo de 50 3D documentos a una escena.
- Los usuarios solo pueden guardar un máximo de 50 3D documentos en una escena.
- Los usuarios también verán una marca de agua de evaluación en las imágenes renderizadas y en todos los demás archivos de salida.
- Cada nodo no puede tener más de 5 nodos secundarios.
- Cada nodo no puede tener más de 2 entidades adjuntas.
- Cada geometría no puede tener más de 2 elementos de vértice adjuntos.
- Cada nodo no puede tener más de 1 material.

{{% alert color="primary" %}} 

Si está utilizando Aspose.3D sin una licencia adecuada, podría**com.aspose.threed.TrialException**Cuando el uso haya alcanzado las restricciones sin licencia, puede desactivar la excepción:

* [Comprar una licencia completa](https://purchase.aspose.com/buy).
* Solicite una licencia temporal de 30 días, consulte [¿Cómo obtener una licencia temporal?](https://purchase.aspose.com/temporary-license) Para obtener más información.
.
* Llame a `com.aspose.threed.TrialException.setSuppressTrialException(true)` antes de sus métodos `open`/`save`, el `TrialException` no se elevará durante la llamada `open`/`save` en Scene, pero las restricciones anteriores no se levantarán.
* Utilice manualmente un bloque `try/catch` en `Scene.open/save`, esta excepción es solo una notificación, ignorarla no afectará la carga/guardado de la escena.

{{% /alert %}} 
##  **Aplicación de una licencia**
La licencia es un archivo XML de texto sin formato que contiene detalles como el nombre del producto, el número de desarrolladores a los que tiene licencia, la fecha de vencimiento de la suscripción, etc. El archivo está firmado digitalmente, por lo que no modifique el archivo; incluso la adición inadvertida de un salto de línea adicional en el archivo lo invalidará. Debe establecer una licencia antes de realizar cualquier operación con documentos. Asegúrese de hacerlo antes de crear un objeto Scene.

Las licencias se pueden aplicar desde varios lugares:

- Trayectoria explícita
- La carpeta que contiene el archivo JAR de Aspose.3D.
- Recurso incrustado en el JAR que se llama Aspose.3D JAR.

Utilice el método `License.setLicense` para licenciar las API. A menudo, la forma más fácil de establecer una licencia es colocar el archivo de licencia en la misma carpeta que el JAR de Aspose.3D y especificar solo el nombre del archivo sin ruta.
###  **Aplicar licencia mediante archivo u objeto Stream**
En este ejemplo Aspose.3D intentará encontrar el archivo de licencia en la carpeta que contiene los JAR de su aplicación.

{{< highlight "java" >}}
License license = new License();
license.setLicense("Aspose._3D.lic");
{{< /highlight >}}

Inicializa una licencia de un stream.

{{< highlight "java" >}}
License license = new License();
try(FileInputStream myStream = new FileInputStream("Aspose._3D.lic")) {
    license.setLicense(myStream);
}
{{< /highlight >}}
###  **Incluyendo el archivo de licencia como recurso incrustado**
Simplemente puede copiar el archivo LIC en la carpeta `resources` de su proyecto. La reconstrucción del proyecto debe incrustar el. Lic en el archivo de la aplicación. Archivo jar. Después de eso, puede aplicar la licencia utilizando el código que se muestra a continuación:

{{< highlight "java" >}}
License lic = new License();
lic.setLicense(Program.class.getResourceAsStream("Aspose.3D.Java.lic"));
{{< /highlight >}}
###  **Validar la licencia**
Es posible validar si la licencia se ha configurado correctamente o no. La clase Licencia tiene el campo isLicente que devolverá true si la licencia se ha establecido correctamente.

{{< highlight "java" >}}
License license = new License();
license.setLicense("Aspose.3D.Java.lic");
    	  
if (License.isLicenseSet()) {
    System.out.println("License is Set!");
}
{{< /highlight >}}
##  **Aplicar Licencia Medida**
Aspose.3D permite a los desarrolladores aplicar la clave medida. Es un nuevo sistema de licencias. El nuevo mecanismo de concesión de licencias se utilizará junto con el método de concesión de licencias existente. Aquellos clientes que desean que se les facture en función del uso de las características API pueden usar la licencia medida. Para más detalles, por favor refiérase a [Preguntas frecuentes sobre Licensing medido](https://purchase.aspose.com/faqs/licensing/metered) sección.

Se ha introducido una nueva clase `Metered` para aplicar la clave medida. A continuación se muestra el código de ejemplo que demuestra cómo establecer la clave pública y privada medida.

{{< highlight "java" >}}
// Initialize a Metered license class object
Metered metered = new Metered();
// Set public and private keys
metered.setMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}
##  **Cuándo aplicar una licencia**
Siga estas simples reglas:

- La licencia solo debe establecerse una vez por dominio de aplicación.
- Debe establecer la licencia antes de usar cualquier otra clase Aspose.3D.
- Llamar a Licencia. SetLicense varias veces no es perjudicial, pero simplemente desperdicia el tiempo del procesador.

Si está desarrollando una biblioteca de clases, puede llamar a License.SetLicense desde un constructor estático de su clase que use Aspose.3D. El constructor estático se ejecutará antes de crear una instancia de su clase asegurándose de que la licencia Aspose.3D esté correctamente establecida.
##  **Puede cambiar el nombre del archivo de licencia**
El nombre del archivo de licencia no tiene que ser 'Aspose.3D.LIC'. Puede cambiarle el nombre a cualquier cosa que desee y usar ese nombre cuando llame a License.SetLicense.
##  **La excepción no puede encontrar el nombre de archivo de licencia**
Cuando compra y descarga una licencia, el sitio web Aspose nombra el archivo de licencia `Aspose.3D.LIC`. Puede descargar el archivo de licencia utilizando su navegador. Algunos exploradores reconocen el archivo de licencia como XML y anexan un archivo. Xml para que el nombre completo del archivo en su computadora se convierta en `Aspose.3D.lic.XML`.

When Microsoft Windows, for example, is configured to hide extensions of known file types (unfortunately this is default in most Windows installations), the license file will appear to you as `Aspose.3D.LIC` in Windows Explorer. You are likely to think this is the real file name and call License.SetLicense passing it `Aspose.3D.LIC`, but there is no such file, hence the exception.

Para resolver el problema, cambie el nombre del archivo para eliminar lo invisible. Extensión xml. También recomendamos que deshabilite la opción "ocultar extensiones" en Microsoft Windows.

##  **Usando múltiples APIs de Aspose**
Si utiliza varias API Aspose en su aplicación, por ejemplo Aspose.3D y Aspose.Cells, aquí hay algunos consejos útiles.

- Establezca la licencia para cada Aspose API por separado. Incluso si tiene un solo archivo de licencia para todas las API, por ejemplo `Aspose.Total.lic`, aún necesita llamar a `License.setLicense` por separado para cada Aspose API que esté utilizando en su aplicación.
- Use el nombre de clase de licencia totalmente calificado. Cada Aspose API tiene una clase License en su espacio de nombres. Por ejemplo, Aspose.3D tiene `com.aspose.3d.License` y Aspose.Cells tiene la clase `com.aspose.cells.License`. El uso del nombre de clase completo le permite evitar cualquier confusión sobre qué licencia se aplica a qué producto.
