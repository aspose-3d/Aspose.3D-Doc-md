---
title: Ejemplo de metadatos estructurales de glTF
type: docs
linkTitle: Metadatos estructurales de glTF
description: Esta página de documentación demuestra cómo leer metadatos estructurales de un archivo glTF usando Aspose.3D para .NET.
weight: 11
---

# Lectura de Metadatos Estructurales desde Archivos glTF

Esta muestra demuestra cómo leer metadatos estructurales de un archivo glTF que contiene la extensión EXT_structural_metadata usando la API de Aspose.3D.

## Explicación del Código

El siguiente código C# carga una escena glTF con metadatos estructurales, luego lee y muestra información sobre las tablas de propiedades y sus propiedades:

```csharp
// Cargar escena glTF con EXT_structural_metadata desde el archivo
var scene = Scene.FromFile("ComplexType.gltf");

// Cargar metadatos estructurales desde la escena
var metadata = StructuralMetadata.From(scene);
Console.WriteLine("Volcado de metadatos estructurales desde el archivo glTF de entrada:");

// Iterar a través de todas las tablas de propiedades en los metadatos
foreach (var propTable in metadata.PropertyTables)
{
    // Obtener la clase meta de la tabla de propiedades
    Console.WriteLine($"Tabla de Propiedades {propTable.Name}, nombre de tipo : {propTable.MetaClass.Name}");

    // Iterar a través de todas las propiedades definidas en la clase meta
    foreach (var propertyDefinition in propTable.MetaClass.Properties)
    {
        // Obtener los datos de la propiedad definidos en EXT_structural_metadata
        object property = propTable.Values[propertyDefinition.Name];
        
        // Volcar el nombre de la propiedad, tipo y valor
        Console.WriteLine($"{propertyDefinition.Name} : {propertyDefinition.Type} = {property}");
    }
}
```

## Conceptos Clave

### Metadatos Estructurales
- La clase `StructuralMetadata` proporciona acceso a los metadatos definidos en la extensión EXT_structural_metadata
- Esta extensión permite almacenar información semántica sobre objetos 3D
- Los metadatos pueden incluir tablas de propiedades que definen atributos para objetos en la escena

### Tablas de Propiedades
- Representadas por la clase `PropertyTable`
- Cada tabla tiene:
  - Un nombre
  - Una clase meta que define la estructura
  - Valores que contienen los datos de propiedad reales

### Clases Meta
- Definidas por la clase `MetaClass`
- Describen la estructura de una tabla de propiedades
- Contienen una colección de definiciones de propiedades
- Cada definición especifica:
  - Nombre de la propiedad
  - Tipo de la propiedad
  - Otros atributos de metadatos

### Acceso a Propiedades
- Las propiedades se acceden a través del diccionario `Values` de una tabla de propiedades
- La clave es el nombre de la propiedad tal como se define en la clase meta
- Los valores se convierten automáticamente a tipos apropiados cuando es posible

Este ejemplo demuestra cómo Aspose.3D se puede usar para leer y procesar metadatos estructurales de archivos glTF, lo que permite a los desarrolladores acceder a información semántica rica almacenada junto con la geometría 3D.