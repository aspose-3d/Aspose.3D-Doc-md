---
title: Especificar opciones de carga de archivos 3D
type: docs
weight: 10
url: "/es/nodejs-java/specify-3d-file-load-options/"
description: Existen varios métodos con sobrecarga de Scene.open o sobrecargas del constructor de la clase Scene que aceptan una instancia de LoadOptions.
---

## **3D File Load Options**
Hay varias sobrecargas del método Scene.open o sobrecargas del constructor de la clase Scene que aceptan una instancia de LoadOptions. Esta debe ser una instancia de una clase derivada de la clase LoadOptions. Cada formato de carga tiene una clase correspondiente que contiene las opciones de carga para ese formato de carga, por ejemplo, existe ColladaSaveOptions para el formato de guardado FileFormat.COLLADA.
### **Uso de las Opciones de Carga de Discreet 3DS**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo Discreet 3DS.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

var loadOpts = new aspose.threed.Discreet3dsLoadOptions();

// Establece si se debe usar la transformación definida en la primera fotograma de la pista de animación.
loadOpts.setApplyAnimationTransform(true);

// Invierte el sistema de coordenadas
loadOpts.setFlipCoordinateSystem(true);

// Prefiere usar color corregido por gamma si un archivo 3ds proporciona tanto el color original como el color corregido por gamma.
loadOpts.setGammaCorrectedColor(true);

{{< /highlight >}}

### **Uso de las Opciones de Carga de Obj**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo 3D Obj.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

var loadObjOpts  = new aspose.threed.ObjLoadOptions();

// Importa materiales desde un archivo de biblioteca de materiales externo
loadObjOpts.setEnableMaterials(true);

// Invierte el sistema de coordenadas.
loadObjOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Uso de las Opciones de Carga de STL**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo STL.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Inicializa un objeto
var loadSTLOpts   = new aspose.threed.StlLoadOptions();

// Invierte el sistema de coordenadas.
loadSTLOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Uso de las Opciones de Carga de U3D**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo U3D.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Inicializa un objeto
var loadU3DOpts = new aspose.threed.U3dLoadOptions();

// Invierte el sistema de coordenadas.
loadU3DOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Uso de las Opciones de Carga de glTF**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo glTF.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Establece las opciones de carga
var loadOpt = new aspose.threed.GltfLoadOptions();

// El valor predeterminado es verdadero, normalmente no necesitamos cambiarlo. Aspose.3D volteará automáticamente la coordenada de textura V/T durante la carga y el guardado.
loadOpt.setFlipTexCoordV(true);

{{< /highlight >}}

### **Uso de las Opciones de Carga de Ply**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un modelo PLY.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// inicializa el objeto de la clase Scene
var scene = new aspose.threed.Scene();

// inicializa un objeto
var loadPLYOpts  = new aspose.threed.PlyLoadOptions();

// Invierte el sistema de coordenadas.
loadPLYOpts.setFlipCoordinateSystem(true);

// carga el modelo 3D Ply
scene.open("vase-v2.ply", loadPLYOpts);

{{< /highlight >}}

### **Uso de las Opciones de Carga de DirectX X**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo DirectX X.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// inicializa el objeto de la clase Scene
var scene = new aspose.threed.Scene();

// inicializa un objeto
var loadXOpts = new aspose.threed.XLoadOptions(aspose.threed.FileContentType.ASCII);

// invierte el sistema de coordenadas.
loadXOpts.setFlipCoordinateSystem(true);

// carga el archivo 3D X
scene.open("warrior.x", loadXOpts);

{{< /highlight >}}

### **Uso de las Opciones de Carga de FBX**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

//Esto imprimirá todas las propiedades definidas en GlobalSettings en el archivo FBX.
var opt = new aspose.threed.FbxLoadOptions();

opt.setKeepBuiltinGlobalSettings(true);

{{< /highlight >}}