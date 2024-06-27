---
title: Fonctionne avec des requêtes d'objet de type XPath
type: docs
weight: 120
url: /fr/net/work-with-xpath-like-object-queries/
description: En utilisant Aspose.3D for .NET, vous pouvez sélectionner un ou plusieurs objets sous le nœud actuel en utilisant la syntaxe de requête XPath-Like. La syntaxe de la requête a été inspirée par XPath, donc la plupart des concepts et de la syntaxe sont similaires, la syntaxe de la requête est compatible avec l'URL, elle sera donc utilisée dans notre version cloud à l'avenir.
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.3 ou supérieure.

{{% /alert %}} 
##  **Fonctionne avec des requêtes d'objet de type XPath**
En utilisant Aspose.3D for .NET, vous pouvez sélectionner un ou plusieurs objets sous le nœud actuel en utilisant la syntaxe de requête XPath-Like. La syntaxe de la requête a été inspirée par XPath, donc la plupart des concepts et de la syntaxe sont similaires, la syntaxe de la requête est compatible avec l'URL, elle sera donc utilisée dans notre version cloud à l'avenir. Habituellement, une syntaxe est composée de**Préfixe Nom Condition** / **Nom Condition** /.

|**Préfixe =**|**Description =**|
| :- | :- |
| // |Sélecteur global, tout descendant est traité comme le nœud racine pour effectuer la sélection|
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

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-XPathLikeObjectQueries-XPathLikeObjectQueries.cs" >}}
