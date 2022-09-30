---
title: Público API Cambios en Aspose.3D 1.3.0
type: docs
weight: 40
url: /es/net/public-api-changes-in-aspose-3d-1-3-0/
---
**Resumen de contenidos**

- [Cambios en el espacio de nombres y el nombre de clase](#PublicAPIChangesinAspose.3D1.3.0-Namespaceandclassnamechanges)
- [Crear vértice mediante la asignación de los modos de referencia y asignación](#PublicAPIChangesinAspose.3D1.3.0-CreateVertexbyAssigningtheReferenceandMappingModes)
- [La opción de guardado Universal 3D se agrega en el formato de archivo](#PublicAPIChangesinAspose.3D1.3.0-Universal3DSavingOptionisaddedintheFileFormat)
- [Incrustar contenido en bruto a la textura de FBX](#PublicAPIChangesinAspose.3D1.3.0-EmbedRawContenttotheTextureofFBX)
- [Se añade el método de descomposición en la clase Matrix4](#PublicAPIChangesinAspose.3D1.3.0-DecomposemethodisaddedintheMatrix4class)
- [Se agrega un nuevo constructor en la clase Vector4 para recibir un parámetro de objeto Vector3](#PublicAPIChangesinAspose.3D1.3.0-AnewconstructorinVector4classisaddedtoreceiveaVector3objectparameter)

{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.3D API de la versión 1.2.0 a 1.3.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.3D.

{{% /alert %}} 
### **Cambios en el espacio de nombres y el nombre de clase**
- Espacio de nombres Aspose.ThreeD. Las animaciones cambiaron a Aspose.ThreeD. Animación
- Clase Aspose.ThreeD. Animación. Animación cambiada a Aspose.ThreeD. Animación. Nodo de animación
- El espacio de nombres Aspose.ThreeD.IO ha cambiado a Aspose.ThreeD. Formatos
- Espacio de nombres Aspose.ThreeD. Se cambiaron a Aspose.ThreeD.Utilities
### **Crear vértice mediante la asignación de los modos de referencia y asignación**
Los desarrolladores pueden crear vértices asignando los modos Referencia y Asignación en una sola línea de código. Código de ejemplo:

{{% alert color="primary" %}} 

El objeto de clase Mesh se está utilizando en el código. Podemos[Crear un objeto de clase Mesh como se narra allí](/pages/createpage.action?spaceKey=3dnet&title=Create+a+3D+Cube+Mesh&linkCreation=true&fromPageId=19923253).

{{% /alert %}} 

**C#**

{{< highlight "csharp" >}}

 // call overloaded CreateElement method of the Mesh object

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;

{{< /highlight >}}

### **La opción de guardado Universal 3D se agrega en el formato de archivo**
La opción de formato Universal 3D se ha agregado en la enum FileFormat. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 // save scene in the Universal3D format

scene.Save("C:\\temp\\Output.fbx", FileFormat.Universal3D);

{{< /highlight >}}

### **Incrustar contenido en bruto a la textura de FBX**
El<tt>Contenido</tt>La propiedad se ha añadido a la<tt>Textura</tt>Para incrustar el contenido en bruto en la textura del documento FBX. Código de ejemplo:

**C#**

{{< highlight "csharp" >}}

 // initialize Texture class object

Texture texture = new Texture();

// set file name

texture.FileName = "embedded-texture.png";

// set binary content

texture.Content = File.ReadAllBytes("c:\\test.png");

{{< /highlight >}}

### **Se añade el método de descomposición en la clase Matrix4**
Es una función de utilidad matemática utilizada para descomponer una matriz de transformación afín.
### **Se agrega un nuevo constructor en la clase Vector4 para recibir un parámetro de objeto Vector3**
Facilita la construcción de un Vector4 basado en el Vector3. El cuarto valor del Vector4 presenta el plano w y su valor predeterminado es 1.
