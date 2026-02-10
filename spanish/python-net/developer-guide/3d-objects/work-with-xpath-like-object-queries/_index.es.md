---
title: Trabajar con consultas de objetos XPath-Like
type: docs
weight: 120
url: /es/python-net/work-with-xpath-like-object-queries/
description: Con Aspose.3D for Python via .NET, puede seleccionar uno o más objetos bajo el nodo actual utilizando la sintaxis de consulta similar a XPath. La sintaxis de consulta se inspiró en XPath, por lo que la mayoría de los conceptos y la sintaxis son similares, la sintaxis de consulta es compatible con la URL, por lo que se utilizará en nuestra versión en la nube en el futuro.
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,3 o superior.

{{% /alert %}} 
##  **Trabajar con consultas de objetos XPath-Like**
Con Aspose.3D for Python via .NET, puede seleccionar uno o más objetos bajo el nodo actual utilizando la sintaxis de consulta similar a XPath. La sintaxis de consulta se inspiró en XPath, por lo que la mayoría de los conceptos y la sintaxis son similares, la sintaxis de consulta es compatible con la URL, por lo que se utilizará en nuestra versión en la nube en el futuro. Por lo general, una sintaxis está compuesta por**Prefijo Nombre Condición** / **Nombre condición** /.

|**Prefijo =**|**Descripción =**|
| :- | :- |
|//|Selector global, cualquier descendiente se trata como el nodo raíz para realizar la selección|
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

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Camera, Light

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
# Create a scene for testing
s = Scene()
a = s.root_node.create_child_node("a")
a.create_child_node("a1")
a.create_child_node("a2")
s.root_node.create_child_node("b")
c = s.root_node.create_child_node("c")
c.create_child_node("c1").add_entity(Camera("cam"))
c.create_child_node("c2").add_entity(Light("light"))
/*The hierarchy of the scene looks like:
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
# select objects that has type Camera or name is 'light' whatever it's located.
objects = s.root_node.select_objects("//*[(@Type = 'Camera') or (@Name = 'light')]")
# Select single camera object under the child nodes of node named 'c' under the root node
c1 = s.root_node.select_single_object("/c/*/<Camera>")
#  Select node named 'a1' under the root node, even if the 'a1' is not a directly child node of the
obj = s.root_node.select_single_object("a1")
# Select the node itself, since the '/' is selected directly on the root node, so the root node is selected.
obj = s.root_node.select_single_object("/")

{{< /highlight >}}
