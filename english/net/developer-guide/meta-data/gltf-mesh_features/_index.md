---
title: "glTF Mesh Features Example"
type: docs
linkTitle: "glTF Mesh Features"
description: "This documentation page demonstrates how to create a glTF file with EXT_mesh_features using Aspose.3D for .NET."
weight: 10
---

# Creating glTF Files with EXT_mesh_features

This sample demonstrates how to create a glTF file with EXT_mesh_features extension using Aspose.3D API.

## Code Explanation

The following C# code creates a mesh with control points and polygons, then adds feature IDs to the control points before saving to a glTF file:

```csharp
// This sample will create a glTF file with EXT_mesh_features
// First we create a mesh
var mesh = new Mesh();

// Add control points (vertices) to the mesh
// The first set of four points creates a square in the XY plane at y=1
mesh.ControlPoints.Add(new Vector4(0, 1, 0));  // Point 0
mesh.ControlPoints.Add(new Vector4(2, 1, 0));  // Point 1
mesh.ControlPoints.Add(new Vector4(2, 2, 0));  // Point 2
mesh.ControlPoints.Add(new Vector4(1, 2, 0));  // Point 3

// The second set of four points creates another square in the XY plane at y=0
mesh.ControlPoints.Add(new Vector4(3, 0, 0));  // Point 4
mesh.ControlPoints.Add(new Vector4(4, 0, 0));  // Point 5
mesh.ControlPoints.Add(new Vector4(4, 1, 0));  // Point 6
mesh.ControlPoints.Add(new Vector4(3, 1, 0));  // Point 7

// Create triangular faces (polygons) from the control points
// First square (points 0-3) is divided into two triangles
mesh.CreatePolygon(0, 1, 2);  // Triangle 0-1-2
mesh.CreatePolygon(0, 2, 3);  // Triangle 0-2-3

// Second square (points 4-7) is also divided into two triangles
mesh.CreatePolygon(4, 5, 6);  // Triangle 4-5-6
mesh.CreatePolygon(4, 6, 7);  // Triangle 4-6-7

// Then we create a user data element to store feature IDs
// This will associate feature IDs with control points
var featureId = (VertexElementUserData)mesh.CreateElement(
    VertexElementType.UserData,  // Element type
    MappingMode.ControlPoint,   // Apply to control points
    ReferenceMode.Direct        // Direct mapping (not indexed)
);

// Assign feature IDs to each control point
// First four points get ID 0, next four get ID 1
featureId.Data = new float[] { 0, 0, 0, 0, 1, 1, 1, 1 };

// Set the special attribute name that conforms to EXT_mesh_features specification
// The format _FEATURE_ID_<n> is recognized by the glTF exporter
featureId.Name = "_FEATURE_ID_0";

// Save the mesh to a glTF Binary (GLB) file
// The exporter will automatically generate the EXT_mesh_features extension data
// Using a relative path for the output file
(new Scene(mesh)).Save("mesh_feature.glb");
```

## Key Concepts

### Mesh Creation
- `Mesh` class represents a polygonal mesh geometry
- Control points define the vertices of the mesh
- `CreatePolygon` method creates triangular faces between control points

### Feature IDs
- Feature IDs allow grouping of geometry within a mesh
- Implemented through `VertexElementUserData` with special naming convention
- `_FEATURE_ID_0` indicates this is a feature ID stream
- Multiple feature ID streams can be created with increasing indices

### Data Assignment
- Feature IDs are stored as float values
- Each control point gets a corresponding feature ID value
- In this example, we use two distinct feature IDs: 0 and 1

### File Export
- Saving to GLB format preserves all features including EXT_mesh_features
- Aspose.3D automatically handles the extension generation
- The resulting file contains metadata about the mesh features
- Using relative paths makes the code more portable and easier to run in different environments

This example demonstrates how Aspose.3D can be used to create glTF files that utilize the EXT_mesh_features extension for advanced 3D data representation.
