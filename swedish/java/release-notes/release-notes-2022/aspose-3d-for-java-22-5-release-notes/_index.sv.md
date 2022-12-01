---
title: Aspose.3D for Java 22,5 Utgivning
type: docs
weight: 8
url: /sv/java/aspose-3d-for-java-22-5-release-notes/
description: Publiceringsnoterna av Aspose.3D for Java 22.5.
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 22.5.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-1149 |Mesh triangulate stöder inte VertexElementUserData med kartläggningsläge Polygon/PolygonVertex|Ny funktion|
|THREEDNET-1148 |Lägg till stöd för VertexElementUserData i TriMesh|Ny funktion|
|THREEDNET-1138 |Tillåt export av VertexElementUserData till glTF|Ny funktion|
|THREEDNET-1119 |Stöd för GLTF egna vertex-attribut|Ny funktion|


## API ändringar ##


### Uppdaterad typ från `Map<String, Object>` till `Object` i klass `com.aspose.threed.VertexElementUserData` :

{{< highlight "java" >}}
    /**
     * The user data attached in this element
     */
    public Object getData();
    
    /**
     * The user data attached in this element
     * @param value New value
     */
    public void setData(Object value);
{{< /highlight >}}


Om gammal kod bifogar flera data i VertexElementUserData, bör nu använda flera VertexElementUserData.

Med detta API ändringar, vi kan stödja konvertera VertexElementUserData till TriMesh eller till och med exporteras till glTF:

Exempelkod:

{{< highlight "csharp" >}}
//Manually define a cube
Vector4[]controlPoints = new Vector4[]{
        new Vector4(-5.0, 0.0, 5.0, 1.0),
        new Vector4(5.0, 0.0, 5.0, 1.0),
        new Vector4(5.0, 10.0, 5.0, 1.0),
        new Vector4(-5.0, 10.0, 5.0, 1.0),
        new Vector4(-5.0, 0.0, -5.0, 1.0),
        new Vector4(5.0, 0.0, -5.0, 1.0),
        new Vector4(5.0, 10.0, -5.0, 1.0),
        new Vector4(-5.0, 10.0, -5.0, 1.0)
};
// Initialize mesh object
Mesh mesh = new Mesh();
// Add control points to the mesh
mesh.getControlPoints().addAll(Arrays.asList(controlPoints));
// Create polygons to mesh
// Front face (Z+)
mesh.createPolygon(0, 1, 2, 3);
// Right side (X+)
mesh.createPolygon(1, 5, 6, 2 );
// Back face (Z-)
mesh.createPolygon(5, 4, 7, 6);
// Left side (X-)
mesh.createPolygon(4, 0, 3, 7);
// Bottom face (Y-)
mesh.createPolygon(0, 4, 5, 1);
// Top face (Y+)
mesh.createPolygon(3, 2, 6, 7 );

//create a user data to store face id for each face, this is done by specifying MappingMode to Polygon
var userData = (VertexElementUserData)mesh.createElement(VertexElementType.USER_DATA, MappingMode.POLYGON, ReferenceMode.DIRECT);
//The name of the UserData will be used as the field's name
userData.setName("__FACE_ID");
userData.setData(new double[]{
        0,1,2,3,4,5
});
var triMesh = TriMesh.fromMesh(mesh);
System.out.println("TriMesh:");
for(var vtx : triMesh)
{
        System.out.println(vtx);
}


{{< /highlight >}}

Utmatningen är:

```
TriMesh:
POSITION = (-5.0,0.0,5.0), __FACE_ID = 0.0
POSITION = (5.0,0.0,5.0), __FACE_ID = 0.0
POSITION = (5.0,10.0,5.0), __FACE_ID = 0.0
POSITION = (5.0,10.0,5.0), __FACE_ID = 0.0
POSITION = (-5.0,10.0,5.0), __FACE_ID = 0.0
POSITION = (5.0,0.0,5.0), __FACE_ID = 1.0
POSITION = (5.0,0.0,-5.0), __FACE_ID = 1.0
POSITION = (5.0,10.0,-5.0), __FACE_ID = 1.0
POSITION = (5.0,10.0,-5.0), __FACE_ID = 1.0
POSITION = (5.0,10.0,5.0), __FACE_ID = 1.0
POSITION = (5.0,0.0,-5.0), __FACE_ID = 2.0
POSITION = (-5.0,0.0,-5.0), __FACE_ID = 2.0
POSITION = (-5.0,10.0,-5.0), __FACE_ID = 2.0
POSITION = (-5.0,10.0,-5.0), __FACE_ID = 2.0
POSITION = (5.0,10.0,-5.0), __FACE_ID = 2.0
POSITION = (-5.0,0.0,-5.0), __FACE_ID = 3.0
POSITION = (-5.0,0.0,5.0), __FACE_ID = 3.0
POSITION = (-5.0,10.0,5.0), __FACE_ID = 3.0
POSITION = (-5.0,10.0,5.0), __FACE_ID = 3.0
POSITION = (-5.0,10.0,-5.0), __FACE_ID = 3.0
POSITION = (-5.0,0.0,5.0), __FACE_ID = 4.0
POSITION = (-5.0,0.0,-5.0), __FACE_ID = 4.0
POSITION = (5.0,0.0,-5.0), __FACE_ID = 4.0
POSITION = (5.0,0.0,-5.0), __FACE_ID = 4.0
POSITION = (5.0,0.0,5.0), __FACE_ID = 4.0
POSITION = (-5.0,10.0,5.0), __FACE_ID = 5.0
POSITION = (5.0,10.0,5.0), __FACE_ID = 5.0
```

