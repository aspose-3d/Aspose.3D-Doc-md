---
title: Fonctionne avec des requêtes d'objet de type XPath
type: docs
weight: 60
url: /fr/java/work-with-xpath-like-object-queries/
description: En utilisant Aspose.3D for Java, vous pouvez sélectionner un ou plusieurs objets sous le nœud actuel en utilisant la syntaxe de requête XPath-Like.
---
##  **Fonctionne avec des requêtes d'objet de type XPath**
En utilisant Aspose.3D for Java, vous pouvez sélectionner un ou plusieurs objets sous le nœud actuel en utilisant la syntaxe de requête XPath-Like. La syntaxe de la requête a été inspirée par XPath, donc la plupart des concepts et de la syntaxe sont similaires, la syntaxe de la requête est compatible avec l'URL, elle sera donc utilisée dans notre version cloud à l'avenir. Habituellement, une syntaxe est composée de**Préfixe Nom Condition** / **Nom Condition** /.

|**Préfixe**|**Description**|
| :- | :- |
| // |Sélecteur global, tout descendant est traité comme le nœud racine pour effectuer la sélection|
|/|Sélecteur racine, un seul ancêtre est utilisé pour lever les yeux|
|Autres|Supposons que c'est un nom et sélectionnez l'objet par nom en mode sélecteur global|

Le nom est une chaîne qui correspond au nom de l'objet, ou un joker `*` est utilisé pour correspondre à n'importe quel nom. La condition est une expression pour décider de sélectionner l'objet, les opérateurs booléens (not) et ou les opérateurs de comparaison `>/</>=/<=/=/!=` sont supportés. Pour accéder à une propriété dans l'expression de condition, le préfixe '@' est utilisé, par exemple, `@Name` lira la propriété Name. Une syntaxe de raccourci pour tester le type est supportée par `<Mesh>`, cela équivaut à `[@Type = 'Mesh']`, les identifiants sans guillemets seront traités comme une chaîne.
###  **Sélectionnez tous les nœuds à l'aide du sélecteur global de syntaxe**
{{< highlight "java" >}}

 //<Node>

{{< /highlight >}}

C'est la courte syntaxe de:

{{< highlight "java" >}}

 //*[<Node>]

{{< /highlight >}}

Ou

{{< highlight "java" >}}

 //*[@Type = Node]

{{< /highlight >}}
###  **Sélectionnez un deuxième nœud de niveau avec un parent visible**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}



Voici l'exemple de code pour interroger un ou plusieurs objets:

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
