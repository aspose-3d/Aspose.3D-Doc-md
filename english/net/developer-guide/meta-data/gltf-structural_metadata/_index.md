---
title: "glTF Structural Metadata Example"
linkTitle: "glTF Structural Metadata"
description: "This documentation page demonstrates how to read structural metadata from a glTF file using Aspose.3D for .NET."
weight: 11
---

# Reading Structural Metadata from glTF Files

This sample demonstrates how to read structural metadata from a glTF file that contains EXT_structural_metadata extension using Aspose.3D API.

## Code Explanation

The following C# code loads a glTF scene with structural metadata, then reads and displays information about property tables and their properties:

```csharp
// Load glTF scene with EXT_structural_metadata from file
var scene = Scene.FromFile("ComplexType.gltf");

// Load structural metadata from scene
var metadata = StructuralMetadata.From(scene);
Console.WriteLine("Dumping structural metadata from input glTF file:");

// Iterate through all property tables in the metadata
foreach (var propTable in metadata.PropertyTables)
{
    // Get the meta class of the property table
    Console.WriteLine($"Property Table {propTable.Name}, type name : {propTable.MetaClass.Name}");

    // Iterate through all properties defined in the meta class
    foreach (var propertyDefinition in propTable.MetaClass.Properties)
    {
        // Get the property data defined in EXT_structural_metadata
        object property = propTable.Values[propertyDefinition.Name];
        
        // Dump the property name, type and value
        Console.WriteLine($"{propertyDefinition.Name} : {propertyDefinition.Type} = {property}");
    }
}
```

## Key Concepts

### Structural Metadata
- The `StructuralMetadata` class provides access to metadata defined in the EXT_structural_metadata extension
- This extension allows storing semantic information about 3D objects
- Metadata can include property tables that define attributes for objects in the scene

### Property Tables
- Represented by the `PropertyTable` class
- Each table has:
  - A name
  - A meta class that defines the structure
  - Values that contain actual property data

### Meta Classes
- Defined by the `MetaClass` class
- Describe the structure of a property table
- Contain a collection of property definitions
- Each definition specifies:
  - Name of the property
  - Type of the property
  - Other metadata attributes

### Property Access
- Properties are accessed through the `Values` dictionary of a property table
- The key is the property name as defined in the meta class
- Values are automatically converted to appropriate types when possible

This example demonstrates how Aspose.3D can be used to read and process structural metadata from glTF files, allowing developers to access rich semantic information stored alongside 3D geometry.