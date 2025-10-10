---
title: "IFC Group Support"
type: docs
linkTitle: "IFC Group Support"
description: "This documentation page demonstrates how to read semantic hierarchy from an IFC file using Aspose.3D for .NET."
weight: 14
---

# IFC Group Support

## Overview

IFC Group is a newly introduced feature in Aspose.3D that enables developers to work with semantic groups defined in IFC files. Unlike the traditional geometric hierarchy, IFC Group provides a way to represent building elements with meaningful grouping, allowing richer data extraction and manipulation.

## What is IFC Group?

In the IFC (Industry Foundation Classes) format, groups are used to create a semantic‑based hierarchy that groups related entities (e.g., walls, doors) under a common identifier. Aspose.3D exposes these groups through the [`Group`](https://reference.aspose.com/3d/net/aspose.threed/group/) class, allowing access to the group's name, semantic information, and child nodes.


## Why Use IFC Group?

Using IFC Group adds semantic context to the otherwise purely geometric scene graph, making it easier to query, filter, and process building elements based on their real‑world meaning. It simplifies tasks such as extracting specific building components, applying material overrides, or generating detailed reports.

## Aspose.3D Support

Aspose.3D provides full support for IFC Group in the .NET API. The following sections show how to enable and work with IFC Groups.

### Accessing Group Information

```csharp
// Load an IFC file
var scene = Aspose.ThreeD.Scene.FromFile("model.ifc");
// Iterate over groups
foreach(Group group in scene2.Library.Where(obj => obj is Group))
{
    Console.WriteLine($"Group Name: {group.Name}");
    Console.WriteLine($" Sub Groups: {group.Groups.Count}");
    Console.WriteLine($" Associated Nodes: {group.Nodes.Count}");
}

```

## Sample Code

The following end‑to‑end example loads an IFC file, and prints the semantic hierarchy:

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");
scene.Open("sample.ifc", loadOptions);

void PrintGroup(Group group, string indent = "")
{
    foreach (var child in group.Groups)
    {
        Console.WriteLine($"{indent}{child.Name}");
        PrintGroup(child, indent + "  ");
    }
}

foreach(Group group in scene2.Library.Where(obj => obj is Group))
{
    PrintGroup(group);
}
```

## References

* [Link to official Aspose.3D IFC documentation](/3d/net/supported-file-formats/ifc)
* [Link to `Aspose.ThreeD.Group`](https://reference.aspose.com/3d/net/aspose.threed/group/)
* [Link to IFC specification](https://technical.buildingsmart.org/standards/ifc/ifc-schema-specifications/)
