---
title: Licencias
type: docs
weight: 60
url: /es/java/licensing/
description: Puede descargar/instalar fácilmente Aspose.3D for Java desde Aspose Repositorio para la evaluación. La descarga de evaluación es la misma que la descarga comprada. La versión de evaluación simplemente tiene licencia cuando agrega algunas líneas de código para aplicar la licencia.
---
## **Evaluar Aspose.3D**
Puede descargar/instalar fácilmente Aspose.3D for Java desde[Aspose Repositorio](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/)Para evaluación. La descarga de evaluación es la misma que la descarga comprada. La versión de evaluación simplemente tiene licencia cuando agrega algunas líneas de código para aplicar la licencia.

La versión de evaluación proporciona todas las características excepto las siguientes:

- Los usuarios solo pueden abrir/importar un máximo de 50 3D documentos a una escena.
- Los usuarios solo pueden guardar un máximo de 50 3D documentos en una escena.
- Los usuarios también verán una marca de agua de evaluación en las imágenes renderizadas y en todos los demás archivos de salida.
- Cada nodo no puede tener más de 5 nodos secundarios.
- Cada nodo no puede tener más de 2 entidades adjuntas.
- Cada geometría no puede tener más de 2 elementos de vértice adjuntos.
- Cada nodo no puede tener más de 1 material.

{{% alert color="primary" %}} 

Si está usando Aspose.3D sin una licencia adecuada, podría desencadenar una**Com aspose! threed! TrialException**Cuando el uso haya alcanzado las restricciones sin licencia, puede desactivar la excepción:

* [Compre una licencia completa](https://purchase.aspose.com/buy).
* Solicite una licencia temporal de 30 días, consulte [¿Cómo obtener una licencia temporal?](https://purchase.aspose.com/temporary-license) Para obtener más información.
.
* Llame a 'com.aspose.threed.TrialException. setSuppressTrialExcepción (verdadero) 'antes de sus métodos 'abierto'/'salvar', la 'TrialException' no se planteará durante la llamada 'abierta'/'salvar' en Scene, pero las restricciones anteriores no se levantarán.
* Utilice manualmente un bloque 'probar/catch' en 'Escena. abrir/guardar', esta excepción es solo una notificación, ignore que no afectará la carga/guardar de la escena.

{{% /alert %}} 
## **Aplicación de una licencia**
La licencia es un archivo XML de texto sin formato que contiene detalles como el nombre del producto, el número de desarrolladores a los que tiene licencia, la fecha de vencimiento de la suscripción, etc. El archivo está firmado digitalmente, por lo que no modifique el archivo; incluso la adición inadvertida de un salto de línea adicional en el archivo lo invalidará. Debe establecer una licencia antes de realizar cualquier operación con documentos. Asegúrese de hacerlo antes de crear un objeto Scene.

Las licencias se pueden aplicar desde varios lugares:

- Trayectoria explícita
- La carpeta que contiene el archivo JAR del Aspose.3D.
- Un recurso incrustado en el JAR que llamó Aspose.3D JAR.

Utilice el método `License.setLicense` para licenciar las API. A menudo, la forma más fácil de establecer una licencia es colocar el archivo de licencia en la misma carpeta que el JAR de Aspose.3D y especificar solo el nombre de archivo sin ruta.
### **Aplicar licencia mediante archivo u objeto Stream**
En este ejemplo, Aspose.3D intentará encontrar el archivo de licencia en la carpeta que contiene los JAR de la aplicación.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingFile.java" >}}

Inicializa una licencia de un stream.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingStreamObject.java" >}}
### **Incluyendo el archivo de licencia como recurso incrustado**
Simplemente puede copiar el archivo LIC en la carpeta `resources` de su proyecto. La reconstrucción del proyecto debería incrustar el. Lic archivo en la solicitud. Archivo jar. Después de eso, puede aplicar la licencia usando el código como el siguiente:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-FileAsEmbeddedResource.java" >}}
### **Validar la licencia**
Es posible validar si la licencia se ha configurado correctamente o no. La clase Licencia tiene el campo isLicente que devolverá true si la licencia se ha establecido correctamente.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ValidateLicense.java" >}}
## **Aplicar Licencia Medida**
Aspose.3D permite a los desarrolladores aplicar la clave medida. Es un nuevo mecanismo de concesión de licencias. El nuevo mecanismo de concesión de licencias se utilizará junto con el método de concesión de licencias existente. Aquellos clientes que quieran ser facturados en función del uso de las funciones API pueden utilizar la licencia medida. Para obtener más detalles, consulte[Preguntas frecuentes sobre licencias métricas](https://purchase.aspose.com/faqs/licensing/metered)Sección.

Se ha introducido una nueva clase `Metered` para aplicar la clave medida. A continuación se muestra el código de muestra que demuestra cómo establecer la clave pública y privada medida.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-PublicAndPrivateKeys.java" >}}
## **Cuándo aplicar una licencia**
Siga estas simples reglas:

- La licencia solo debe establecerse una vez por dominio de aplicación.
- Debe establecer la licencia antes de usar cualquier otra clase Aspose.3D.
- Llamar a Licencia. SetLicense varias veces no es perjudicial, pero simplemente desperdicia el tiempo del procesador.

Si está desarrollando una biblioteca de clases, puede llamar a Licencia. SetLicense de un constructor estático de su clase que utiliza Aspose.3D. El constructor estático se ejecutará antes de que se cree una instancia de su clase, asegurándose de que la licencia Aspose.3D está correctamente establecida.
## **Puede cambiar el nombre del archivo de licencia**
El nombre del archivo de licencia no tiene que ser 'Aspose.3D.LIC'. Puede cambiarle el nombre a cualquier cosa que desee y usar ese nombre cuando llame a License.SetLicense.
## **La excepción no puede encontrar el nombre de archivo de licencia**
Cuando compra y descarga una licencia, el sitio web Aspose nombra el archivo de licencia `Aspose.3D.LIC`. Puede descargar el archivo de licencia utilizando su navegador. Algunos navegadores reconocen el archivo de licencia como XML y anexan un archivo. Extensión xml para que el nombre completo del archivo en su ordenador sea `Aspose.3D.lic.XML`.

Cuando Microsoft Windows, por ejemplo, está configurado para ocultar extensiones de tipos de archivos conocidos (desafortunadamente esto es predeterminado en la mayoría de las instalaciones Windows), el archivo de licencia le aparecerá como `Aspose.3D.LIC` en Windows Explorer. Es probable que piense que este es el nombre de archivo real y llame a Licencia. SetLicense pasándolo `Aspose.3D.LIC`, pero no existe tal archivo, de ahí la excepción.

Para resolver el problema, cambie el nombre del archivo para eliminar el invisible. Extensión xml. También recomendamos que desactive la opción "ocultar extensiones" en Microsoft Windows.

## **Uso de múltiples API de Aspose**
Si utiliza varias APIs Aspose en su aplicación, por ejemplo, Aspose.3D y Aspose.Cells, aquí hay algunos consejos útiles.

- Establezca la licencia para cada Aspose API por separado. Incluso si tiene un único archivo de licencia para todas las API, por ejemplo, `Aspose.Total.lic`, aún necesita llamar al `License.setLicense` por separado para cada Aspose API que esté utilizando en su aplicación.
- Utilice el nombre de la clase de licencia totalmente calificado. Cada Aspose API tiene una clase de licencia en su espacio de nombres. Por ejemplo, Aspose.3D tiene `com.aspose.3d.License` y Aspose.Cells tiene `com.aspose.cells.License` clase. El uso del nombre de clase completo le permite evitar cualquier confusión sobre qué licencia se aplica a qué producto.
