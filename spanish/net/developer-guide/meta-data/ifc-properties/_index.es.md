---
description: "Esta página de documentación muestra cómo leer propiedades de un archivo IFC usando Aspose.3D para .NET."
linkTitle: "Soporte de propiedades IFC"
title: "Soporte de propiedades IFC"
type: docs
weight: 14
---
## Visión general

El Soporte de Propiedades IFC es una característica de Aspose.3D que permite a los desarrolladores leer conjuntos de propiedades y cantidades de elementos definidas en archivos IFC. Estas propiedades se almacenan en las entidades `IFCPROPERTYSET` y `IFCELEMENTQUANTITY` y pueden accederse mediante el método `A3DObject.GetProperty`.

## ¿Qué es el Soporte de Propiedades IFC?

En el esquema IFC, los elementos de construcción pueden tener asociados conjuntos de propiedades (`IFCPROPERTYSET`) y cantidades de elementos (`IFCELEMENTQUANTITY`). Aspose.3D los mapea a una interfaz de propiedad genérica, exponiéndolos vía `A3DObject.GetProperty(string propertyName)`. Esto permite recuperar valores como clasificación de incendio, transmitancia térmica o cantidades de material directamente del modelo 3D.

## ¿Por qué usar el Soporte de Propiedades IFC?

* Acceder a datos semánticos ricos sin analizar manualmente el archivo IFC.  
* Habilitar procesos posteriores como estimación de costos, verificación de cumplimiento o exportación de datos.  
* Combinar información geométrica y no geométrica en un único flujo de trabajo.

## Soporte de Aspose.3D

El siguiente ejemplo en C# muestra cómo cargar un archivo IFC y leer una propiedad:

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");

// Encontrar un elemento específico, p. ej., una pared
var wallNode = scene.RootNode.Children.FirstOrDefault(n => n.Name == "Wall_123");

// Recuperar un valor de propiedad
if (wallNode != null)
{
    // Nombre de la propiedad tal como está definido en el archivo IFC
    var fireRating = wallNode.GetProperty("ifc:FireRating");
    Console.WriteLine($"Fire Rating: {fireRating}");

    // Ejemplo de cantidad de elemento
    var volume = wallNode.GetProperty("ifc:GrossVolume");
    Console.WriteLine($"Gross Volume: {volume}");
}
```

### Notas

* Los nombres de las propiedades definidos en un archivo IFC llevan el prefijo `ifc:` para evitar conflictos con propiedades nativas.  
* Los nombres de las propiedades distinguen entre mayúsculas y minúsculas y deben coincidir exactamente con los definidos en el archivo IFC.  
* `GetProperty` devuelve un `object`; conviértalo al tipo apropiado (p. ej., `double`, `string`) según sea necesario.  
* Este código de ejemplo muestra la recuperación de propiedades desde `Node`; sin embargo, cualquier descendiente de `A3DObject` puede usar `GetProperty`.  
* Si una propiedad no existe, `GetProperty` devuelve `null`.

## Referencias

* [Enlace a la documentación oficial de Aspose.3D IFC](/3d/net/supported-file-formats/ifc)  
* Enlace a [`Aspose.ThreeD.A3DObject`](https://reference.aspose.com/3d/net/aspose.threed/a3dobject/)  
* Especificación IFC para `IFCPROPERTYSET` y `IFCELEMENTQUANTITY`