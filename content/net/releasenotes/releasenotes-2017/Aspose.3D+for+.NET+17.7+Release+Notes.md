+++
title = "Aspose.3D for .NET 17.7 Release Notes" 
description = "" 
weight = 12132 
+++

Aspose.3D for .NET : Aspose.3D for .NET 17.7 Release Notes  

# Aspose.3D for .NET : Aspose.3D for .NET 17.7 Release Notes


This page contains release notes for [Aspose.3D for .NET 17.7](https://www.nuget.org/packages/Aspose.3D/17.7.0).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-265|Add support of exporting 3D scene to PLY format.|New feature|
|THREEDNET-271|Simplify the creation of transform matrix.|New feature|
|THREEDNET-270|Allow generate mesh from grayscale image as a height map.|New feature|
|THREEDNET-272|The FBX file generated cannot be edited by 3ds max.|Bug|
|THREEDNET-274|UVs are corrupted when exporting a scene in FBX format.|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).

#### Adds Members to Aspose.ThreeD.Utilities.Matrix4 Class

**C#**

{{< code lang="c#" >}}
/// <summary>
/// Creates a translation matrix 
/// </summary>
/// <param name="t"></param>
/// <returns></returns>
public static Matrix4 Translate(Vector3 t);
/// <summary>
/// Creates a translation matrix 
/// </summary>
/// <param name="tx"></param>
/// <param name="ty"></param>
/// <param name="tz"></param>
/// <returns></returns>
public static Matrix4 Translate(double tx, double ty, double tz);
/// <summary>
/// Create a scale matrix
/// </summary>
/// <param name="s"></param>
/// <returns></returns>
public static Matrix4 Scale(Vector3 s);

/// <summary>
/// Create a scale matrix
/// </summary>
/// <param name="s"></param>
/// <returns></returns>
public static Matrix4 Scale(double s);

/// <summary>
/// Create a scale matrix
/// </summary>
/// <param name="sx"></param>
/// <param name="sy"></param>
/// <param name="sz"></param>
/// <returns></returns>
public static Matrix4 Scale(double sx, double sy, double sz);

/// <summary>
/// Create a rotation matrix from euler angle
/// </summary>
/// <param name="eul">Rotation in radian</param>
/// <returns></returns>
public static Matrix4 RotateFromEuler(Vector3 eul);
/// <summary>
/// Create a rotation matrix from euler angle
/// </summary>
/// <param name="rx">Rotation in x axis in radian</param>
/// <param name="ry">Rotation in y axis in radian</param>
/// <param name="rz">Rotation in z axis in radian</param>
/// <returns></returns>
public static Matrix4 RotateFromEuler(double rx, double ry, double rz) 

/// <summary>
/// Create a rotation matrix by rotation angle and axis
/// </summary>
/// <param name="angle">Rotate angle in radian</param>
/// <param name="axis">Rotation axis</param>
/// <returns></returns>
public static Matrix4 Rotate(double angle, Vector3 axis);

/// <summary>
/// Create a rotation matrix from a quaternion
/// </summary>
/// <param name="rotate"></param>
/// <returns></returns>
public static Matrix4 Rotate(Quaternion rotate);
 
//Create a transform that translates (1, 0, 0) then rotates alone the y axis pi radian.
var m  = Matrix4.RotateFromEuler(0, Math.PI, 0) * Matrix4.Translate(1, 0, 0);
{{< /code >}}

#### Adds new classes Aspose.ThreeD.Utilities.ComposeOrder and Aspose.ThreeD.Utilities.TransformBuilder

The transform builder simplifies the creation of the transformation matrix by a chain of operations.

**C#**

{{< code lang="c#" >}}
//use prepend order so the calculation is performed from left to right:
var m = (new TransformBuilder(ComposeOrder.Prepend))
    //Change the (x, y, z) into (x + 1, y, z)
    .Translate(1, 0, 0)
    //Rotate alone with the Y axis with 180deg will change the (x, y, z) into (-x, y, -z)
    .RotateEulerDegree(0, 180, 0)
    //Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)
    .Scale(2)
    //change the (x, y, z) into (z, y, x)
    .Rearrange(Axis.ZAxis, Axis.YAxis, Axis.XAxis)
    .Matrix;
    
//Apply this matrix on a (0, 0, 0) vector, then we get the right result (0, 0, -2)
var t = m * Vector3.Origin;
{{< /code >}}

#### Members updated to Aspose.ThreeD.Formats

This change introduces a new class Aspose.ThreeD.Formats.PlyFormat, which allows you to encode single mesh instead of the whole scene:

**C#**

{{< code lang="c#" >}}
public static readonly Aspose.ThreeD.FileFormat PLY;
//Changed to
public static readonly Aspose.ThreeD.Formats.PlyFormat PLY;
 
// sample code
// Create a cylinder object and save it to ply file
FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply");
{{< /code >}}

#### Adds a new class Aspose.ThreeD.Formats.PlySaveOptions

Ply format has no an official standard, different application may have different definitions of its vertex format, this class allows you to define details of the Ply format.  
For example the default component name for texture coordinate components is 'u' and 'v', but some application uses 's' and 't', then you can change the name by using this class:

**C#**

{{< code lang="c#" >}}
//Save as binary PLY format, the default value is ASCII
PlySaveOptions opt = new PlySaveOptions(FileContentType.Binary);
//change the components to 's' and 't'
opt.TextureCoordinateComponents.Item1 = "s";
opt.TextureCoordinateComponents.Item2 = "t";
//save the mesh
FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply", opt);
{{< /code >}}

### Usage Examples

Please check the list of help topics added or updated in the Aspose.3D Wiki docs:

1.  [Convert Mesh of a single 3D object in PLY file](https://docs2.aspose.com/3d/net/developerguide/3dobjects/convert+mesh+of+a+single+3d+object+in+ply+file)
2.  [Simplify the creation of transformation matrix by the chain operations](https://docs2.aspose.com/3d/net/developerguide/geometry/simplify+the+creation+of+transformation+matrix+by+the+chain+operations)

