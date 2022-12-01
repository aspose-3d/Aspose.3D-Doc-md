---
title: Aspose.3D for .NET 22,5 Utgivning
type: docs
weight: 8
url: /sv/net/aspose-3d-for-net-22-5-release-notes/
description: Publiceringsnoterna av Aspose.3D for .NET 22.5.
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 22.5.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-1149 |Mesh triangulate stöder inte VertexElementUserData med kartläggningsläge Polygon/PolygonVertex|Ny funktion|
|THREEDNET-1148 |Lägg till stöd för VertexElementUserData i TriMesh|Ny funktion|
|THREEDNET-1138 |Tillåt export av VertexElementUserData till glTF|Ny funktion|
|THREEDNET-1119 |Stöd för GLTF egna vertex-attribut|Ny funktion|


## API ändringar ##


### Uppdaterad typ av fastighet från `Dictionary<String, Object>` till `object` i klass `Aspose.ThreeD.Entities.VertexElementUserData`:

{{< highlight "csharp" >}}
        /// <summary>
        /// The user data attached in this element
        /// </summary>
        public object Data { get; set; }
{{< /highlight >}}


Om gammal kod bifogar flera data i `VertexElementUserData`, bör nu använda flera `VertexElementUserData`.

Med detta API ändringar, vi kan stödja konvertera `VertexElementUserData` till `TriMesh` eller till och med exporteras till glTF:

Exempelkod:

{{< highlight "csharp" >}}
//Manually define a cube
Vector4[]controlPoints = new Vector4[]{
        new Vector4( -5.0, 0.0, 5.0, 1.0),
        new Vector4( 5.0, 0.0, 5.0, 1.0),
        new Vector4( 5.0, 10.0, 5.0, 1.0),
        new Vector4( -5.0, 10.0, 5.0, 1.0),
        new Vector4( -5.0, 0.0, -5.0, 1.0),
        new Vector4( 5.0, 0.0, -5.0, 1.0),
        new Vector4( 5.0, 10.0, -5.0, 1.0),
        new Vector4( -5.0, 10.0, -5.0, 1.0)
};
// Initialize mesh object
Mesh mesh = new Mesh();
// Add control points to the mesh
mesh.ControlPoints.AddRange(controlPoints);
// Create polygons to mesh
// Front face (Z+)
mesh.CreatePolygon(new int[]{ 0, 1, 2, 3 });
// Right side (X+)
mesh.CreatePolygon(new int[]{ 1, 5, 6, 2 });
// Back face (Z-)
mesh.CreatePolygon(new int[]{ 5, 4, 7, 6 });
// Left side (X-)
mesh.CreatePolygon(new int[]{ 4, 0, 3, 7 });
// Bottom face (Y-)
mesh.CreatePolygon(new int[]{ 0, 4, 5, 1 });
// Top face (Y+)
mesh.CreatePolygon(new int[]{ 3, 2, 6, 7 });

//create a user data to store face id for each face, this is done by specifying MappingMode to Polygon
var userData = (VertexElementUserData)mesh.CreateElement(VertexElementType.UserData, MappingMode.Polygon, ReferenceMode.Direct); ;
//The name of the UserData will be used as the field's name
userData.Name = "__FACE_ID";
userData.Data = new double[]{
        0,1,2,3,4,5
};
var triMesh = TriMesh.FromMesh(mesh);
Console.WriteLine("TriMesh:");
foreach(var vtx in triMesh)
{
        Console.WriteLine(vtx);
}

{{< /highlight >}}

Utmatningen är:

```
TriMesh:
Position = (-5,0,5), __FACE_ID = 0
Position = (5,0,5), __FACE_ID = 0
Position = (5,10,5), __FACE_ID = 0
Position = (5,10,5), __FACE_ID = 0
Position = (-5,10,5), __FACE_ID = 0
Position = (5,0,5), __FACE_ID = 1
Position = (5,0,-5), __FACE_ID = 1
Position = (5,10,-5), __FACE_ID = 1
Position = (5,10,-5), __FACE_ID = 1
Position = (5,10,5), __FACE_ID = 1
Position = (5,0,-5), __FACE_ID = 2
Position = (-5,0,-5), __FACE_ID = 2
Position = (-5,10,-5), __FACE_ID = 2
Position = (-5,10,-5), __FACE_ID = 2
Position = (5,10,-5), __FACE_ID = 2
Position = (-5,0,-5), __FACE_ID = 3
Position = (-5,0,5), __FACE_ID = 3
Position = (-5,10,5), __FACE_ID = 3
Position = (-5,10,5), __FACE_ID = 3
Position = (-5,10,-5), __FACE_ID = 3
Position = (-5,0,5), __FACE_ID = 4
Position = (-5,0,-5), __FACE_ID = 4
Position = (5,0,-5), __FACE_ID = 4
Position = (5,0,-5), __FACE_ID = 4
Position = (5,0,5), __FACE_ID = 4
Position = (-5,10,5), __FACE_ID = 5
Position = (5,10,5), __FACE_ID = 5
Position = (5,10,-5), __FACE_ID = 5
Position = (5,10,-5), __FACE_ID = 5
Position = (-5,10,-5), __FACE_ID = 5
```

