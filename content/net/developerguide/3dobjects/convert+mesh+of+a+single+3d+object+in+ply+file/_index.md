---
title : "Convert Mesh of a single 3D object in PLY file" 
description : "" 
weight : 12040 
toc : false
type: docs
url: /net/developerguide/3dobjects/convert+mesh+of+a+single+3d+object+in+ply+file/
---

# Aspose.3D for .NET : Convert Mesh of a single 3D object in PLY file


[Aspose.3D for .NET](https://www.aspose.com/products/3d/net) API allows developers to convert the Mesh of a single 3D object in the PLY file.

## Create a 3D object and save it to PLY file

The overloaded EncodeMesh members exposed by the PlyFormat class can be used to convert the Mesh of a 3D object to PLY file. The EncodeMesh members take the Mesh, output file name and PlySaveOptions objects as parameters. Using the PLY save options, developers can change the name of coordinate components.

### Programming Sample 

This code example creates a 3D Cylinder object, and then encode in the PLY file.

**C#**

{{< code lang="c#" >}}
// Create a cylinder object and save it to ply file
FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply");
/* using Ply save options*/
//Save as binary PLY format, the default value is ASCII
PlySaveOptions opt = new PlySaveOptions(FileContentType.Binary);
//change the components to 's' and 't'
opt.TextureCoordinateComponents.Item1 = "s";
opt.TextureCoordinateComponents.Item2 = "t";
//save the mesh
FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply", opt);
{{< /code >}}

