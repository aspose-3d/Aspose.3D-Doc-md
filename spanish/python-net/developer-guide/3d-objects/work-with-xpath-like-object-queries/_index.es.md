---
title: Trabajar con consultas de objetos XPath-Like
type: docs
weight: 120
url: /es/python-net/work-with-xpath-like-object-queries/
description: Con Aspose.3D para Python via .NET, puede seleccionar uno o más objetos en el nodo actual mediante la sintaxis de consulta XPath-Like. La sintaxis de la consulta se inspiró en XPath, por lo que la mayoría de los conceptos y la sintaxis son similares, la sintaxis de la consulta es compatible con la URL, por lo que se utilizará en nuestra versión en la nube en el futuro.
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,3 o superior.

{{% /alert %}} 
## **Trabajar con consultas de objetos XPath-Like**
Con Aspose.3D para Python via .NET, puede seleccionar uno o más objetos en el nodo actual mediante la sintaxis de consulta XPath-Like. La sintaxis de la consulta se inspiró en XPath, por lo que la mayoría de los conceptos y la sintaxis son similares, la sintaxis de la consulta es compatible con la URL, por lo que se utilizará en nuestra versión en la nube en el futuro. Por lo general, una sintaxis está compuesta por**Prefijo Nombre Condición** / **Nombre condición** /.

|**Prefijo =**|**Descripción =**|
|:- |:- |
|//|Selector global, cualquier descendiente se trata como el nodo raíz para realizar la selección|
|/|Selector de raíz, solo se usa un antepasado para buscar|
|Otros|Suponga que es un nombre y seleccione el objeto por nombre en el modo de selector global|
El nombre es una cadena que coincide con el nombre del objeto, o el comodín `*` se utiliza para coincidir con cualquier nombre. La condición es una expresión para decidir si seleccionar el objeto, se admiten los operadores booleanos (no) y, o bien, los operadores de comparación `>/</>=/<=/=/!=`. Para acceder a una propiedad en la expresión de condición, se usa el prefijo '@', por ejemplo, `@Name` leerá la propiedad Name. `<Mesh>` admite una sintaxis de acceso directo para el tipo de prueba, esto es equivalente a `[@Type = 'Mesh']`, los identificadores sin cotización se tratarán como una cadena.
### **Seleccione todos los nodos utilizando el selector global de sintaxis**
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
### **Seleccione un nodo de segundo nivel con un padre visible**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}

A continuación se muestra el código de ejemplo para consultar uno o más objetos:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-XPathLikeObjectQueries-XPathLikeObjectQueries.py" >}}
