---
title: Aspose.3D for Java 22.5 Note di rilascio
type: docs
weight: 8
url: /it/java/aspose-3d-for-java-22-5-release-notes/
description: Le note di rilascio dello Aspose.3D for Java 22.5.
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 22.5.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-1149 |La triangolata mesh non supporta VertexElementUserData con la modalità di mappatura Polygon/PolygonVertex|Nuova funzione|
|THREEDNET-1148 |Aggiungere il supporto di VertexElementUserData in TriMesh|Nuova funzione|
|THREEDNET-1138 |Consenti l'esportazione di VertexElementUserData in glTF|Nuova funzione|
|THREEDNET-1119 |Supporto per gli attributi Vertex personalizzati GLTF|Nuova funzione|


## API modifiche ##


### Aggiornato il tipo di proprietà dallo `Map<String, Object>` allo `Object` nella classe `com.aspose.threed.VertexElementUserData`:

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


Se il vecchio codice allega più dati in VertexElementUserData, ora dovrebbe utilizzare più VertexElementUserData.

Con queste modifiche API, possiamo supportare la conversione di VertexElementUserData in TriMesh o addirittura esportata in glTF:

Esempio di codice:

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

L'output è:

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

