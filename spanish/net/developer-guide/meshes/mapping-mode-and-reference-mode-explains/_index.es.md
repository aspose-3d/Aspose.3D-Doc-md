---
title: Explica mappingmode y ReferenceMode
type: docs
weight: 10
url: /es/net/mapping-mode-and-reference-mode-explains
description: Usando Aspose.3D for .NET, los desarrolladores pueden definir malla con varios elementos de datos de vértice, aquí explicamos cómo asignar datos al componente de mallas y resuzar datos.
---
{{% alert color="primary" %}}

Usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), los desarrolladores pueden definir mallas con varios elementos de datos de vértice, incluyendo normales, colores y pesos. Aspose.3D ofrece dos mecanismos para optimizar la reutilización de datos: `MappingMode` y `ReferenceMode`. Estos mecanismos están diseñados para minimizar la huella de memoria de las mallas, particularmente en formatos avanzados como FBX y USD. MappingMode permite una asignación eficiente de datos de vértice a componentes de malla, mientras que ReferenceMode facilita la referencia de datos de elementos de vértice en varios componentes de malla. Juntas, estas características mejoran el rendimiento y la eficiencia de la memoria, haciendo de Aspose.3D una poderosa herramienta para manejar modelos complejos de 3D en aplicaciones de .NET.

{{% /alert %}}



###  `MappingMode` explica

 `MappingMode` determina cómo se asignan los datos del elemento a la superficie de la geometría en Aspose.3D for .NET. Proporciona varias formas de definir esta asignación:

1. **Punto de control**Cada elemento de datos se asigna al punto de control de la geometría. Este modo garantiza que cada punto de control, que define la forma de la geometría, esté asociado con un elemento de datos específico.
1. **Poligonvértice**Los datos se asignan al vértice de un polígono. En los casos en que un punto de control es compartido por múltiples polígonos, cada instancia del punto de control, tal como aparece en diferentes polígonos, tendrá sus propios datos distintos. Esto garantiza que incluso los puntos de control compartidos pueden tener datos únicos cuando sirven como vértices para diferentes polígonos.
1. **Polígono**Los datos se asignan a todo el polígono. Esto significa que todos los vértices de un polígono comparten el mismo elemento de datos. Este modo es útil cuando es necesario aplicar datos uniformes en toda la superficie del polígono, lo que garantiza la coherencia dentro del polígono.
1. **Borde**, Los datos se asignan a los bordes de la geometría. Cada extremo de un borde comparte los mismos datos, lo que proporciona una forma de aplicar datos uniformes a los bordes al tiempo que permite datos distintos para diferentes bordes. Esto puede ser particularmente útil para definir características que son específicas de los bordes, como valores de pliegue o atributos basados en el borde
1. **AllSame**Un único elemento de datos se asigna a toda la superficie de la geometría. Independientemente de si los datos se interpretan como puntos de control, vértices de polígono o extremos de borde, el mismo valor de datos se aplica de manera uniforme en todos los elementos. Este modo es ideal para escenarios donde se necesita mantener un valor constante en toda la geometría, asegurando un atributo uniforme en todo el modelo 3D.




###  `ReferenceMode` explica
 `ReferenceMode` define si se deben reutilizar los datos por índices, hay tres políticas para `ReferenceMode`:

1.**Directo**, Los datos se referencian directamente y se almacenan en la propiedad `Data` de `VertexElement`.
1.**IndexToDirect**, Los datos se hace referencia por índice, luego se accede por índice en la lista de datos de `VertexElement`.
1.**Índice**, Los datos solo están referenciados por el índice, ahora solo el `VertexElementMaterial` usa este modo de referencia, esto es similar a `IndexToDirect` pero las diferencias son los materiales se definen bajo la propiedad `Node` `Materials`, no en `VertexElementMaterial`, all `VertexElement` sólo funciona con datos primitivos.



Por ejemplo, dada una definición de un cubo:

{{< highlight "csharp" >}}
var cube = new Mesh();
Vector4[] controlPoints = new Vector4[]
{
    new Vector4( -5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 10.0, -5.0, 1.0),
    new Vector4( -5.0, 10.0, -5.0, 1.0)
};
cube.ControlPoints.AddRange(controlPoints);

// Front face (Z+)
cube.CreatePolygon(new int[] { 0, 1, 2, 3 });
// Right side (X+)
cube.CreatePolygon(new int[] { 1, 5, 6, 2 });
// Back face (Z-)
cube.CreatePolygon(new int[] { 5, 4, 7, 6 });
// Left side (X-)
cube.CreatePolygon(new int[] { 4, 0, 3, 7 });
// Bottom face (Y-)
cube.CreatePolygon(new int[] { 0, 4, 5, 1 });
// Top face (Y+)
cube.CreatePolygon(new int[] { 3, 2, 6, 7 });

var vertexColor = (VertexElementVertexColor) cube.CreateElement(VertexElementType.VertexColor);
vertexColor.MappingMode = MappingMode.ControlPoint;
var red = new Vector4(1, 0, 0, 1);
var green = new Vector4(0, 1, 0, 1);
var blue = new Vector4(0, 0, 1, 1);
var white = new Vector4(1, 1, 1, 1);

{{< /highlight >}}

Si desea asignar rojo a los puntos de control 0 y 1, verde a los puntos de control 2 y 3, azul a los puntos de control 4 y 5 y blanco a los puntos de control 6 y 7, puede lograr esto con el siguiente enfoque:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.Direct;
vertexColor.Data.Add(red); // 0
vertexColor.Data.Add(red); // 1
vertexColor.Data.Add(green); // 2
vertexColor.Data.Add(green); // 3
vertexColor.Data.Add(blue); // 4
vertexColor.Data.Add(blue); // 5
vertexColor.Data.Add(white); // 6
vertexColor.Data.Add(white); // 7
{{< /highlight >}}

Para asignar colores a los puntos de control de forma eficaz y reducir el consumo de memoria, puede utilizar índices para hacer referencia a los colores. Al definir los colores por separado y luego hacer referencia a ellos con índices, puede minimizar la redundancia. He aquí cómo puedes lograr esto:

Primero, defina 4 colores en el tipo Vector4 para los colores únicos, y luego use una matriz de 8 índices para asignar estos colores a cada punto de control:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.IndexToDirect;
vertexColor.Data.Add(red);
vertexColor.Data.Add(green);
vertexColor.Data.Add(blue);
vertexColor.Data.Add(white);

vertexColor.SetIndices(new int[] { 0, 0, 1, 1, 2, 2, 3, 3 });
{{< /highlight >}}

En este enfoque:

1. Definir colores únicos: solo se definen 4 colores (rojo, verde, azul, blanco) como instancias de Vector4.
1. Crear una matriz de índice de color: se utiliza una matriz de 8 índices para hacer referencia a estos 4 colores para cada punto de control.
1. Asigne colores usando índices: al hacer referencia a los colores a través de índices, reduce el consumo de memoria, ya que cada color se almacena una vez y se reutiliza en múltiples puntos de control.

Este método optimiza el uso de la memoria al reducir el almacenamiento de datos redundante, lo que hace que su modelo 3D sea más eficiente.