---
title: Работа с XPath-подобными объектными запросов
type: docs
weight: 120
url: /ru/net/work-with-xpath-like-object-queries/
description: Используя Aspose.3D for .NET, вы можете выбрать один или несколько объектов в текущем узле, используя синтаксис запроса XPath-Like. Синтаксис запроса был вдохновлен XPath, поэтому большинство концепций и синтаксиса похожи, синтаксис запроса совместим с URL, поэтому он будет использоваться в нашей облачной версии в будущем.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,3 или выше.

{{% /alert %}} 
##  **Работа с XPath-подобными объектными запросов**
Используя Aspose.3D for .NET, вы можете выбрать один или несколько объектов в текущем узле, используя синтаксис запроса XPath-Like. Синтаксис запроса был вдохновлен XPath, поэтому большинство концепций и синтаксиса похожи, синтаксис запроса совместим с URL, поэтому он будет использоваться в нашей облачной версии в будущем. Как правило, синтаксис состоит из**Условие имени префикса** / **Имя Состояние** /.

|**Префикс =**|**Описание =**|
| :- | :- |
| // |Глобальный селектор, любой потомок рассматривается как корневой узел для выполнения выбора|
|/|Корневой селектор, только один предок используется для поиска|
|Другие|Предположим, что это имя, и выберите объект по имени в глобальном режиме селектора|
Имя-это строка, которая соответствует имени объекта, или подстановочный знак `*` используется для сопоставления любого имени. Условие является выражением, определяющим, следует ли выбирать объект, поддерживаются логические операторы (не) и/или операторы сравнения `>/</>=/<=/=/!=`. Для доступа к свойству в выражении условия используется префикс '@', например, `@Name` будет читать свойство Name. Синтаксис ярлыка для тестируемого типа поддерживается `<Mesh>`, это эквивалентно `[@Type = 'Mesh']`, идентификаторы без кавычки будут рассматриваться как строка.
###  **Выберите все узлы, используя глобальный селектор синтаксиса**
{{< highlight "java" >}}

 //<Node>

{{< /highlight >}}

Это короткий синтаксис:

{{< highlight "java" >}}

 //*[<Node>]

{{< /highlight >}}

Или

{{< highlight "java" >}}

 //*[@Type = Node]

{{< /highlight >}}
###  **Выберите узел второго уровня с видимым родителем**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}

Ниже приводится пример кода для запроса одного или нескольких объектов:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
//Create a scene for testing 
Scene s = new Scene();
var a = s.RootNode.CreateChildNode("a");
a.CreateChildNode("a1");
a.CreateChildNode("a2");
s.RootNode.CreateChildNode("b");
var c = s.RootNode.CreateChildNode("c");
c.CreateChildNode("c1").AddEntity(new Camera("cam"));
c.CreateChildNode("c2").AddEntity(new Light("light"));
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
//select objects that has type Camera or name is 'light' whatever it's located.
var objects = s.RootNode.SelectObjects("//*[(@Type = 'Camera') or (@Name = 'light')]");
//Select single camera object under the child nodes of node named 'c' under the root node
var c1 = s.RootNode.SelectSingleObject("/c/*/<Camera>");
// Select node named 'a1' under the root node, even if the 'a1' is not a directly child node of the 
var obj = s.RootNode.SelectSingleObject("a1");
//Select the node itself, since the '/' is selected directly on the root node, so the root node is selected.
obj = s.RootNode.SelectSingleObject("/");

{{< /highlight >}}
