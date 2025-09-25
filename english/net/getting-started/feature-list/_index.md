---
title: Feature List
type: docs
weight: 30
url: /net/feature-list/
description: General Features and Feature Matrix for C# .NET 3D File Manipulation and Conversion API.
---

Aspose.3D for .NET Features - 3D file manipulation and conversion API built in C#.

## **General Features**
- Written completely in C#, works with .NET Framework.
- .NET environment required.
- Supports Windows Forms and ASP.NET applications.
- API reference in HTML and Microsoft Help format.
- Supported .NET Frameworks (2.0, 3.5, 4.0, 4.0_ClientProfile, 4.5.0, 4.5.1, 4.6.0, 4.6.2, 4.7, 4.7.2).
- 32-bit OS support.
- 64-bit OS support.

## **Feature Matrix**

|**Features** |`FBX` | `Collada` | `glTF` | `glTF 2.0` | `U3D` | `PDF` | `STL` | `OBJ` | `PLY` | `3DS` | `ASE` | `X` | `3MF` | `RVM` | `Draco` |
| :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- |
|` `Lambert Material |![](accept.png) |![](accept.png) |![](accept.png) | |![](accept.png) |![](accept.png) | |![](accept.png) | |![](accept.png) |![](accept.png) |![](accept.png) | | | |
|` `Phong Material |![](accept.png) |![](accept.png) |![](accept.png) | |![](accept.png) |![](accept.png) | |![](accept.png) | | |![](accept.png) |![](accept.png) | | | |
|` `Shader-based Material |![](accept.png) | |![](accept.png) | | | | | | | | | | | | |
|` `PBR Material | | | |![](accept.png) | | | | | | | | | | | |
|` `PBR Specular Material | | | |![](accept.png) | | | | | | | | | | | |
|` `Diffuse texture |![](accept.png) |![](accept.png) | |![](accept.png) |![](accept.png) |![](accept.png) | |![](accept.png) | |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) | | |
|` `Advanced texture |![](accept.png) |![](accept.png) | |![](accept.png) |![](accept.png) |![](accept.png) | |![](accept.png) | | | | | | | |
|` `Polygon meshes |![](accept.png) |![](accept.png) | | | | | |![](accept.png) | | | | | |![](accept.png) | |
|` `Triangle-based meshes |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |
|` `Vertex elements |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) | |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) | | |![](accept.png) |
|` `NURBS geometries |![](accept.png) | | | | | | | | | | | | | | |
|` `Parameterized geometries | | | | | | | | | | | | | |![](accept.png) | |
|` `Local transformation |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) | | | |![](accept.png) |![](accept.png) |![](accept.png) | |![](accept.png) | |
|` `Instancing |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) | | | | | | | | | |
|` `Scene graph |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) |![](accept.png) | | | |![](accept.png) | |![](accept.png) | |![](accept.png) | |
|` `Custom property |![](accept.png) | |![](accept.png) |![](accept.png) | | | | | | | | | | | |
|` `Skeleton |![](accept.png) |![](accept.png) | | | | | | | | | | | | | |
|` `Morph deformer |![](accept.png) |![](accept.png) | | | | | | | | | | | | | |
|` `Property animation |![](accept.png) |![](accept.png) | | | | | | | | | | | | | |
|` `Mesh Compression |![](accept.png) | | | |![](accept.png) |![](accept.png) | | | | | | |![](accept.png) | |![](accept.png) |

## **Supported glTF 2.0 Extensions**

Aspose.3D for .NET provides comprehensive support for key glTF 2.0 extensions:

### Core glTF 2.0 Features
- Base glTF 2.0 format with JSON-based scene description
- Binary container format (GLB) for efficient delivery
- Material system supporting physically based rendering (PBR)

### glTF Extension Support

#### KHR_draco_mesh_compression
- Enables loading and saving of compressed meshes
- Reduces file size significantly with minimal performance impact
- Ideal for web-based applications requiring efficient transmission

#### EXT_mesh_features
- Supports advanced mesh feature grouping
- Allows associating feature IDs with geometry elements
- Enables rich visualization and processing capabilities

#### EXT_structural_metadata
- Provides access to structured semantic information
- Supports property tables with typed attributes
- Allows storage of custom metadata alongside geometry

#### KHR_materials_common
- Includes common material presets
- Simplifies creation of standard materials
- Ensures cross-platform compatibility

#### KHR_materials_pbrSpecularGlossiness
- Supports legacy PBR material workflows
- Maintains compatibility with existing content pipelines
- Provides alternative PBR parameterization