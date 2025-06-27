---
title: "How to Split Mesh by HalfSpace in Aspose.3D"
type: docs
linkTitle: "Split Mesh by HalfSpace"
description: "Learn how to split 3D meshes using HalfSpace planes in Aspose.3D"
weight: 10
---

# Splitting Meshes by HalfSpace in Aspose.3D

This tutorial demonstrates how to use Aspose.3D to perform mesh splitting operations using HalfSpace planes. This technique is useful for extracting specific portions of a 3D model based on spatial criteria.

## Understanding HalfSpace Operations

A HalfSpace represents an infinite space divided by a plane. When combined with Aspose.3D's boolean operations, it allows you to extract specific portions of a mesh that exist on one side of the defined plane.

### Key Concepts:
- **HalfSpace**: Represents an infinite space divided by a plane
- **Boolean Operations**: Used to extract mesh portions relative to the HalfSpace
- **Plane Equation**: Defined as ax + by + cz + d = 0, where (a,b,c) is the normal vector
- **Positive Side**: The portion of space where the plane normal points to

## Code Example: Splitting a Mesh with HalfSpace

The following C# code demonstrates how to create a simple box mesh and split it using a HalfSpace plane:

```csharp
using System;
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;
using Aspose.ThreeD.Utilities;

class MeshBooleanWithHalfSpace
{
    public static void Execute()
    {
        // Create a new 3D scene
        Scene scene = new Scene();
        
        // Create a box mesh (2x2x2 dimensions by default)
        Mesh boxMesh = (new Box()).ToMesh();
        Node boxNode = scene.RootNode.CreateChildNode("Box", boxMesh);
        
        // Create HalfSpace cutting plane
        HalfSpace halfSpace = new HalfSpace();
        
        // Define plane equation: ax + by + cz + d = 0
        // Using plane normal pointing in Z-direction
        halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
        
        // Position the HalfSpace (create node and transform)
        Node halfSpaceNode = scene.RootNode.CreateChildNode("HalfSpace", halfSpace);
        halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);  // Position at z=0.5
        
        // Perform boolean split operation
        Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
        
        // Add result to scene and save
        scene.RootNode.CreateChildNode("SplitResult", splitResult.Entity);
        scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
        
        Console.WriteLine("Mesh split using HalfSpace completed successfully.");
    }
}
```

## Code Explanation

### Namespace Requirements
```csharp
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;  // Contains HalfSpace and BooleanOperator classes
using Aspose.ThreeD.Utilities; // Contains Vector3 and Plane utilities
```

### Creating the Geometry
1. **Scene Initialization**: `Scene scene = new Scene();`
2. **Box Creation**: `(new Box()).ToMesh()` creates a standard cube
3. **Node Hierarchy**: Mesh is added to the scene through a child node

### Defining the Cutting Plane
1. **Plane Definition**:
   ```csharp
   halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
   ```
   - Creates a horizontal XY plane at z=0
   - Normal vector (0,0,1) points upward

2. **Positioning**:
   ```csharp
   halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);
   ```
   - Moves the cutting plane to z=0.5
   - Affects which portion of the mesh is retained

### Performing the Operation
```csharp
Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
```
- Returns the portion of mesh on the positive side of the plane
- Result is added back to the scene hierarchy

### Saving the Result
```csharp
scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
```
- Supported formats include OBJ, STL, FBX, GLTF, and more
- Only the split fragment is saved, not the original mesh

## Visualizing the Operation

### Original Box Dimensions:
- Spans from (-1,-1,-1) to (1,1,1)
- Centered at the origin

### With Plane at z=0.5:
- Keeps portion where z > 0.5 (top part of box)
- Discards portion where z < 0.5 (bottom part)

## Advanced Usage

### Getting Both Sides of the Cut
```csharp
// Original split (positive side)
Node positiveFragment = BooleanOperator.Split(boxNode, halfSpaceNode);

// Invert plane for negative side
halfSpace.Plane = new Plane(new Vector3(0, 0, -1), 0);
Node negativeFragment = BooleanOperator.Split(boxNode, halfSpaceNode);
```

### Adjusting the Cutting Plane
```csharp
// Different orientation - angled cut
halfSpace.Plane = new Plane(new Vector3(0.707, 0, 0.707), 0);
halfSpaceNode.Transform.Translation = new Vector3(0, 0, 1);
```

This implementation demonstrates the core functionality of Aspose.3D's mesh splitting capabilities using HalfSpace planes, allowing for precise extraction of 3D geometry based on spatial criteria.