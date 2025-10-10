---
title: "IFC Property Support"
type: docs
linkTitle: "IFC Property Support"
description: "This documentation page demonstrates how to read properties from an IFC file using Aspose.3D for .NET."
weight: 14
---
## Overview

IFC Property Support is a feature in Aspose.3D that allows developers to read property sets and element quantities defined in IFC files. These properties are stored in `IFCPROPERTYSET` and `IFCELEMENTQUANTITY` entities and can be accessed through the `A3DObject.GetProperty` method.

## What is IFC Property Support?

In the IFC schema, building elements can have associated property sets (`IFCPROPERTYSET`) and element quantities (`IFCELEMENTQUANTITY`). Aspose.3D maps these to a generic property interface, exposing them via `A3DObject.GetProperty(string propertyName)`. This enables retrieval of values such as fire rating, thermal transmittance, or material quantities directly from the 3D model.

## Why Use IFC Property Support?

* Access rich semantic data without parsing the IFC file manually.  
* Enable downstream processes such as cost estimation, compliance checking, or data export.  
* Combine geometric and non‑geometric information in a single workflow.

## Aspose.3D Support

The following C# example demonstrates how to load an IFC file and read a property:

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");

// Find a specific element, e.g., a wall
var wallNode = scene.RootNode.Children.FirstOrDefault(n => n.Name == "Wall_123");

// Retrieve a property value
if (wallNode != null)
{
    // Property name as defined in the IFC file
    var fireRating = wallNode.GetProperty("ifc:FireRating");
    Console.WriteLine($"Fire Rating: {fireRating}");

    // Example of element quantity
    var volume = wallNode.GetProperty("ifc:GrossVolume");
    Console.WriteLine($"Gross Volume: {volume}");
}
```

### Notes

* Property names defined in an IFC file are prefixed with `ifc:` to avoid conflicts with native properties.
* Property names are case‑sensitive and must match the names defined in the IFC file.  
* `GetProperty` returns an `object`; cast to the appropriate type (e.g., `double`, `string`) as needed.  
* This sample code demonstrates retrieving properties from `Node`; however, any descendant of `A3DObject` can use `GetProperty`.
* If a property does not exist, `GetProperty` returns `null`.

## References

* [Link to official Aspose.3D IFC documentation](/3d/net/supported-file-formats/ifc)
* Link to [`Aspose.ThreeD.A3DObject`](https://reference.aspose.com/3d/net/aspose.threed/a3dobject/)
* IFC specification for `IFCPROPERTYSET` and `IFCELEMENTQUANTITY`