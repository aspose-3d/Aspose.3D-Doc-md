---
title: Aspose.3D for Java 20,4 Utgivning
type: docs
weight: 40
url: /sv/java/aspose-3d-for-java-20-4-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller release anteckningar för Aspose.3D for Java 20.4.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-663 |` `Lägg Linux renderingsstöd|` `Ny funktion|
|THREEDNET-661 |` ` Hämta data med egna VertexDeclarationer|` `Förbättring|
|THREEDNET-652 |` `Lägg till omloppsrörelsekontroll.|` `Förbättring|
|THREEDNET-653 |` `Lägg till linjestöd i A3DW format.|` `Förbättring|
|THREEDNET-655 |` `Lägg till renderingsstöd för TriMesh|` `Förbättring|
|THREEDNET-656 |` `Ljusgivning var felaktig i webben återgivning.|` `Bug|
## **Offentlig API och bakåtkompatibla förändringar**
### **Lagt till medlemmar i klassen com.aspose. Threed.utilities.Vertex**
Läs fältets data från en vertex.

{{< highlight "java" >}}

 /**

\* Read the vector4 field

\* @param field The field with a Vector4/FVector4 data type

*/

public Vector4 readVector4(VertexField field);

/**

\* Read the vector4 field

\* @param field The field with a Vector4/FVector4 data type

*/

public FVector4 readFVector4(VertexField field);

/**

\* Read the vector3 field

\* @param field The field with a Vector3/FVector3 data type

*/

public Vector3 readVector3(VertexField field);

/**

\* Read the vector3 field

\* @param field The field with a Vector3/FVector3 data type

*/

public FVector3 readFVector3(VertexField field);

/**

\* Read the vector2 field

\* @param field The field with a Vector2/FVector2 data type

*/

public Vector2 readVector2(VertexField field);

/**

\* Read the vector2 field

\* @param field The field with a Vector2/FVector2 data type

*/

public FVector2 readFVector2(VertexField field);

/**

\* Read the double field

\* @param field The field with a float/double compatible data type

*/

public double readDouble(VertexField field);

/**

\* Read the float field

\* @param field The field with a float/double compatible data type

*/

public float readFloat(VertexField field);

{{< /highlight >}}
#### **Urvalskod**
{{< highlight "java" >}}

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

{{< /highlight >}}
### **Lagt medlem till klass com.aspose. Threed.entities.TriMesh**
Om dina TriMesh instanser kommer med en osäker minnes layout, du kan använda den här metoden för att skapa en ny instans med exakt behövd minnes layout.



{{< highlight "java" >}}

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

{{< /highlight >}}
### **Lagt medlem till klass com.aspose. Threed.entities.TriMesh**
Med denna metod kan du enkelt rekonstruera TriMesh-exempel från en byte array, som deserialisering.

{{< highlight "java" >}}

 /**

 * Create TriMesh from raw data

 * @param vd Vertex declaration, must contains at least one field.

 * @param vertices The input vertex data, the minimum length of the vertices must be greater or equal to vertex declaration's size

 * @param indices The triangle indices

 * @param generateVertexMapping Generate {@link com.aspose.threed.Vertex} for each vertex, which is not necessary for just serialization/deserialization.

 * @return The {@link com.aspose.threed.TriMesh} instance that encapsulated the input byte array.

 */

public static TriMesh fromRawData(VertexDeclaration vd, byte[]vertices, int[]indices, boolean generateVertexMapping)

{{< /highlight >}}
#### **Exempel användning**
{{< highlight "java" >}}

 Scene s = new Scene("test.stl");

Mesh mesh = (Mesh)s.getRootNode().getChildNodes().get(0).getEntity();

VertexDeclaration vd = new VertexDeclaration();

VertexField pos = vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.POSITION);

VertexField normal = vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.NORMAL);

VertexField uv = vd.addField(VertexFieldDataType.F_VECTOR2, VertexFieldSemantic.UV);

TriMesh originalTriMesh = TriMesh.fromMesh(vd, mesh);

//If the original TriMesh's memory layout is not what you wanted, you can use CopyFrom to get a new instance

//with specified memory layout

byte[]verticesInBytes = originalTriMesh.verticesToArray();

int[][]indices = new int[1][];

originalTriMesh.indicesToArray(indices);

TriMesh m = TriMesh.fromRawData(vd, verticesInBytes, indices[0], true);

for(Vertex vtx : m)

{

	Vector3 v_pos = vtx.readVector3(pos);

	Vector3 v_normal = vtx.readVector3(normal);

	Vector2 v_uv = vtx.readVector2(uv);

	System.out.printf("(%s), (%s), (%s)\n", v_pos, v_normal, v_uv);

}

{{< /highlight >}}
#### **Tillagd klass com.aspose. Threed.render.WindowHandle.**
Det här används för att inkapsla det infödda fönstret för att skapa ett renderingsfönster.
### **Tilläggs medlem i klassen com.aspose. Threed.render.renderfactory**
{{< highlight "java" >}}

 /**

\* Create a render target that renders to the native window.

\* @param parameters Render parameters to create the render window

\* @param handle The handle of the window to render

*/

public abstract IRenderWindow createRenderWindow(RenderParameters parameters, WindowHandle handle);

{{< /highlight >}}

Den gamla.*Skapa ombyggd fönsterName*Är märkt som Deprecated, för att anpassa den gamla koden till denna metod, rätta din gamla kod som följande kod snippet.

{{< highlight "java" >}}

 //Renderer renderer = ... your renderer instance

//RenderParameters renderParameters = ... your render parameters

//Control control = ... your control for rendering.

//window = renderer.getRenderFactory().createRenderWindow(new RenderParameters(), shell.handle);

//The above code should be fixed like the following line, pass a Win32 handle.

window = renderer.getRenderFactory().createRenderWindow(new RenderParameters(), WindowHandle.fromWin32(shell.handle));

{{< /highlight >}}
### **Lagt till medlemmar i klassen com.aspose. Threed.utilities.IOUtils**
Dessa är utökningsmetoder för att skriva Vector2/Vector3 till BinaryWriter.



{{< highlight "java" >}}

 /**

\* Write the vector to the binary writer

\* @param writer Target binary writer

\* @param v Vector to write

*/

public static void write(BinaryWriter writer, Vector2 v)

   throws IOException;

/**

\* Write the vector to the binary writer

\* @param writer Target binary writer

\* @param v Vector to write

*/

public static void write(BinaryWriter writer, Vector3 v)

   throws IOException;

{{< /highlight >}}
### **Lagt till medlemmar till klass aspose. Threed.utilities.vector3**
Dessa är matematiska verktyg för att beräkna vinkeln i radian mellan två vektorer i 3D utrymme.

{{< highlight "java" >}}

 /**

\* Calculate the inner angle between two direction

\* Two direction can be non-normalized vectors

\* @param dir The direction vector to compare with

\* @param up The up vector of the two direction's shared plane

\* @return inner angle in radian

*/

public double angleBetween(Vector3 dir, Vector3 up);

/**

\* Calculate the inner angle between two direction

\* Two direction can be non-normalized vectors

\* @param dir The direction vector to compare with

\* @return inner angle in radian

*/

public double angleBetween(Vector3 dir);

{{< /highlight >}}
















