---
title: Trabajar con consultas de objetos XPath-Like
type: docs
weight: 60
url: /es/java/work-with-xpath-like-object-queries/
description: Usando Aspose.3D for Java, puede seleccionar uno o más objetos bajo el nodo actual usando la sintaxis de consulta similar a XPath.
---
##  **Trabajar con consultas de objetos XPath-Like**
Usando Aspose.3D for Java, puede seleccionar uno o más objetos bajo el nodo actual usando la sintaxis de consulta similar a XPath. La sintaxis de consulta se inspiró en XPath, por lo que la mayoría de los conceptos y la sintaxis son similares, la sintaxis de consulta es compatible con la URL, por lo que se utilizará en nuestra versión en la nube en el futuro. Por lo general, una sintaxis está compuesta por**Prefijo Nombre Condición** / **Nombre condición** /.

|**Prefijo**|**Descripción**|
| :- | :- |
| // |Selector global, cualquier descendiente se trata como el nodo raíz para realizar la selección|
|/|Selector de raíz, solo se usa un antepasado para buscar|
|Otros|Suponga que es un nombre y seleccione el objeto por nombre en el modo de selector global|

El nombre es una cadena que coincide con el nombre del objeto, o el comodín `*` se utiliza para que coincida con cualquier nombre. La condición es una expresión para decidir si se debe seleccionar el objeto, se admiten los operadores booleanos (not) y/o los operadores de comparación `>/</>=/<=/=/!=`. Para acceder a una propiedad en la expresión de condición, se usa el prefijo '@', por ejemplo, `@Name` leerá la propiedad Name. Una sintaxis de acceso directo para el tipo de prueba es compatible con `<Mesh>`, esto es equivalente a `[@Type = 'Mesh']`, los identificadores sin cita se tratarán como una cadena.
###  **Seleccione todos los nodos utilizando el selector global de sintaxis**
{{< highlight "java" >}}

 //<Node>

{{< /highlight >}}

Esta es la sintaxis corta de:

{{< highlight "java" >}}

 //*[<Node>]

{{< /highlight >}}

O

{{< highlight "java" >}}

 //*[@Type = Node]

{{< /highlight >}}
###  **Seleccione un nodo de segundo nivel con un padre visible**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}



A continuación se muestra el código de ejemplo para consultar uno o más objetos:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
//Create a scene for testing
Scene s = new Scene();
// Create a child node
Node a = s.getRootNode().createChildNode("a");
// Create a sub-child node
a.createChildNode("a1");
// Create a sub-child node
a.createChildNode("a2");
// Create a child node
s.getRootNode().createChildNode("b");
// Create a child node
Node c = s.getRootNode().createChildNode("c");
// Create a sub-child node
c.createChildNode("c1").addEntity(new Camera("cam"));
// Create a sub-child node
c.createChildNode("c2").addEntity(new Light("light"));
/*
The hierarchy of the scene looks like:
 - Root
    - a
        - a1
        - a2
    - b
    - c
        - c1
            - cam
        - c2
            - light
             */
//select objects that has type Camera or name is 'light' whatever it's located.
List<A3DObject> objects = s.getRootNode().selectObjects("//*[(@Type = 'Camera') or (@Name = 'light')]");

//Select single camera object under the child nodes of node named 'c' under the root node
A3DObject c1 = s.getRootNode().selectSingleObject("/c/*/<Camera>");

// Select node named 'a1' under the root node, even if the 'a1' is not a directly child node of the
A3DObject obj = s.getRootNode().selectSingleObject("a1");

//Select the node itself, since the '/' is selected directly on the root node, so the root node is selected.
obj = s.getRootNode().selectSingleObject("/");

{{< /highlight >}}
