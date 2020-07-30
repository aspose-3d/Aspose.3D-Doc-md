---
title : "Aspose.3D for Java 20.4 Release Notes" 
description : "" 
weight : 12055 
toc : false
type: docs
url: /java/releasenotes/2020/aspose.3d+for+java+20.4+release+notes/
---

# Aspose.3D for Java : Aspose.3D for Java 20.4 Release Notes


This page contains release notes information for Aspose.3D for Java 20.4.

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-663 | Add Linux rendering support | New feature |
|THREEDNET-661 | Get data with custom VertexDeclaration | Enhancement |
|THREEDNET-652 | Add orbital movement control | Enhancement |
|THREEDNET-653 | Add line support in A3DW format. | Enhancement |
|THREEDNET-655 | Add rendering support of TriMesh | Enhancement |
|THREEDNET-656 | Light rendering was incorrect in web renderer. | Bug|
{{< /table >}}

## Public API and Backward Incompatible Changes

### Added members to class com.aspose.threed.utilities.Vertex

Read the field's data from a vertex.

{{< code lang="cs" >}}
/**
* Read the vector4 field
* @param field The field with a Vector4/FVector4 data type
*/
public Vector4 readVector4(VertexField field);

/**
* Read the vector4 field
* @param field The field with a Vector4/FVector4 data type
*/
public FVector4 readFVector4(VertexField field);

/**
* Read the vector3 field
* @param field The field with a Vector3/FVector3 data type
*/
public Vector3 readVector3(VertexField field);

/**
* Read the vector3 field
* @param field The field with a Vector3/FVector3 data type
*/
public FVector3 readFVector3(VertexField field);

/**
* Read the vector2 field
* @param field The field with a Vector2/FVector2 data type
*/
public Vector2 readVector2(VertexField field);

/**
* Read the vector2 field
* @param field The field with a Vector2/FVector2 data type
*/
public FVector2 readFVector2(VertexField field);

/**
* Read the double field
* @param field The field with a float/double compatible data type
*/
public double readDouble(VertexField field);

/**
* Read the float field
* @param field The field with a float/double compatible data type
*/
public float readFloat(VertexField field);
{{< /code >}}

#### Sample Code

{{< code lang="cs" >}}
Scene s = new Scene("test.stl");
Mesh mesh = (Mesh)s.getRootNode().getChildNodes().get(0).getEntity();
//create a VertexDeclaration so we can get the TriMesh with memory layout exactly we want.
VertexDeclaration vd = new VertexDeclaration();

VertexField pos = vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.POSITION);
VertexField normal = vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.NORMAL);
VertexField uv = vd.addField(VertexFieldDataType.F_VECTOR2, VertexFieldSemantic.UV);

//construct the TriMesh using specified vertex layout
TriMesh m = TriMesh.fromMesh(vd, mesh);
//print each vertex's position, normal and uv
for(Vertex vtx : m)
{
	Vector3 v_pos = vtx.readVector3(pos);
	Vector3 v_normal = vtx.readVector3(normal);
	Vector2 v_uv = vtx.readVector2(uv);
	System.out.printf("(%s), (%s), (%s)\n", v_pos, v_normal, v_uv);
}
{{< /code >}}

### Added member to class com.aspose.threed.entities.TriMesh

If your TriMesh instances come with an uncertain memory layout, you can use this method to construct a new instance with exactly needed memory layout.

{{< code lang="cs" >}}
Scene s = new Scene("test.STL");
var mesh = (Mesh)s.RootNode.ChildNodes[0].Entity;
var originalTriMesh = TriMesh.FromMesh(mesh);

//create a VertexDeclaration so we can get the TriMesh with memory layout exactly we want.
VertexDeclaration vd = new VertexDeclaration();

VertexField pos = vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.POSITION);
VertexField normal = vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.NORMAL);
VertexField uv = vd.addField(VertexFieldDataType.F_VECTOR2, VertexFieldSemantic.UV);

//If the original TriMesh's memory layout is not what you wanted, you can use CopyFrom to get a new instance
//with specified memory layout

TriMesh m = TriMesh.copyFrom(originalTriMesh, vd);
//print each vertex's position, normal and uv
for(Vertex vtx : m)
{
	Vector3 v_pos = vtx.readVector3(pos);
	Vector3 v_normal = vtx.readVector3(normal);
	Vector2 v_uv = vtx.readVector2(uv);
	System.out.printf("(%s), (%s), (%s)\n", v_pos, v_normal, v_uv);
}
{{< /code >}}

### Added member to class com.aspose.threed.entities.TriMesh

With this method, you can easily reconstruct the TriMesh instance from a byte array, like deserialization.

{{< code lang="cs" >}}
/**
 * Create TriMesh from raw data
 * @param vd Vertex declaration, must contains at least one field.
 * @param vertices The input vertex data, the minimum length of the vertices must be greater or equal to vertex declaration's size
 * @param indices The triangle indices
 * @param generateVertexMapping Generate {@link com.aspose.threed.Vertex} for each vertex, which is not necessary for just serialization/deserialization.
 * @return The {@link com.aspose.threed.TriMesh} instance that encapsulated the input byte array.
 */
public static TriMesh fromRawData(VertexDeclaration vd, byte[] vertices, int[] indices, boolean generateVertexMapping)
{{< /code >}}

#### Example Usage

{{< code lang="cs" >}}
Scene s = new Scene("test.stl");
Mesh mesh = (Mesh)s.getRootNode().getChildNodes().get(0).getEntity();
VertexDeclaration vd = new VertexDeclaration();

VertexField pos = vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.POSITION);
VertexField normal = vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.NORMAL);
VertexField uv = vd.addField(VertexFieldDataType.F_VECTOR2, VertexFieldSemantic.UV);

TriMesh originalTriMesh = TriMesh.fromMesh(vd, mesh);

//If the original TriMesh's memory layout is not what you wanted, you can use CopyFrom to get a new instance
//with specified memory layout

byte[] verticesInBytes = originalTriMesh.verticesToArray();
int[][] indices = new int[1][];
originalTriMesh.indicesToArray(indices);
TriMesh m = TriMesh.fromRawData(vd, verticesInBytes, indices[0], true);

for(Vertex vtx : m)
{
	Vector3 v_pos = vtx.readVector3(pos);
	Vector3 v_normal = vtx.readVector3(normal);
	Vector2 v_uv = vtx.readVector2(uv);
	System.out.printf("(%s), (%s), (%s)\n", v_pos, v_normal, v_uv);
}
{{< /code >}}

#### Added class com.aspose.threed.render.WindowHandle

This is used to encapsulate the native window handle for creating a render window.

### Added member to class com.aspose.threed.render.renderfactory

{{< code lang="cs" >}}
/**
* Create a render target that renders to the native window.
* @param parameters Render parameters to create the render window
* @param handle The handle of the window to render
*/
public abstract IRenderWindow createRenderWindow(RenderParameters parameters, WindowHandle handle);
{{< /code >}}

The old *createRenderWindow* is marked as Deprecated, to port the old code to this method, fix your old code like the following code snippet.

{{< code lang="cs" >}}
//Renderer renderer = ... your renderer instance
//RenderParameters renderParameters = ... your render parameters
//Control control = ... your control for rendering.

//window = renderer.getRenderFactory().createRenderWindow(new RenderParameters(), shell.handle);
//The above code should be fixed like the following line, pass a Win32 handle.
window = renderer.getRenderFactory().createRenderWindow(new RenderParameters(), WindowHandle.fromWin32(shell.handle));
{{< /code >}}

### Added members to class com.aspose.threed.utilities.IOUtils

These are extension methods for writing Vector2/Vector3 to BinaryWriter.

{{< code lang="cs" >}}
/**
* Write the vector to the binary writer
* @param writer Target binary writer
* @param v Vector to write
*/
public static void write(BinaryWriter writer, Vector2 v)
   throws IOException;

/**
* Write the vector to the binary writer
* @param writer Target binary writer
* @param v Vector to write
*/
public static void write(BinaryWriter writer, Vector3 v)
   throws IOException;
{{< /code >}}

### Added members to class aspose.threed.utilities.vector3

These are mathematical utilities for calculating the angle in radian between two vectors in 3D space.

{{< code lang="cs" >}}
/**
* Calculate the inner angle between two direction
* Two direction can be non-normalized vectors
* @param dir The direction vector to compare with
* @param up The up vector of the two direction's shared plane
* @return inner angle in radian
*/
public double angleBetween(Vector3 dir, Vector3 up);

/**
* Calculate the inner angle between two direction
* Two direction can be non-normalized vectors
* @param dir The direction vector to compare with
* @return inner angle in radian
*/
public double angleBetween(Vector3 dir);
{{< /code >}}

