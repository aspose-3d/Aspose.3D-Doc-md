---
title: IFC support
type: docs
weight: 1
url: /net/supported-file-formats/ifc
description: C# .NET 3D File Manipulation and Conversion API can load and save 3DS, 3MF, AMF, FBX, DFX, OBJ, PLY, STL, USD, U3D and other formats
tags: ifc
---

# IFC Support

## Overview
Aspose.3D for .NET can import IFC files just like other 3D formats. The IFC file is parsed and represented as a regular 3D scene, allowing you to work with geometry, materials, and semantic data.

### What is IFC?
Industry Foundation Classes (IFC) is an open, neutral data model developed by buildingSMART to describe, exchange, and share building and construction industry data. It captures both geometric information (shapes, coordinates) and rich semantic data (materials, properties, relationships) about building elements.

### IFC Versions
- **IFC2x3** – Early widely adopted version, provides basic geometry and property sets.
- **IFC4** – Introduced improved schema, support for more building elements, enhanced property definitions, and better interoperability.
- **IFC4.1 / IFC4.2** – Incremental updates adding new entity definitions, improved MVDs (Model View Definitions), and expanded support for infrastructure.
- **IFC4.3** – Latest version (as of 2025) with further extensions for infrastructure, facility management, and detailed material specifications.

These versions are all supported by Aspose.3D, allowing you to load IFC files regardless of the schema version.

## Importing IFC
```csharp
using Aspose.ThreeD;

// Load an IFC file
var scene = Scene.FromFile("building.ifc");

// The scene now contains nodes, meshes, and metadata.
```

## Property Sets
IFC property sets are exposed via `A3DObject.GetProperty`. Property names are prefixed with `ifc:` to avoid conflicts.

```csharp
var wall = scene.RootNode.Children.FirstOrDefault(n => n.Name == "Wall_1");
var fireRating = wall?.GetProperty("ifc:FireRating");
Console.WriteLine($"Fire Rating: {fireRating}");
```

## IFC Grouping
Semantic groups defined in IFC are accessible through the `Group` class.

```csharp
foreach (var group in scene.Library.Where(o => o is Group))
{
    var g = (Group)group;
    Console.WriteLine($"Group: {g.Name}, Nodes: {g.Nodes.Count}");
}
```

## Additional Features
- Access to element quantities (`ifc:GrossVolume`, etc.).
- Case‑sensitive property names.
- `GetProperty` returns `object`; cast to appropriate type.

## References
- [Aspose.3D API References](https://reference.aspose.com/3d/net/)
- [IFC Specification](https://technical.buildingsmart.org/standards/ifc/ifc-schema-specifications/)
- [IFC Group Support](/3d/net/developer-guide/meta-data/ifc-group/)
- [IFC Property Support](/3d/net/developer-guide/meta-data/ifc-properties/)
