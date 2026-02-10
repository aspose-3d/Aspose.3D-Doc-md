---
title: Работа с XPath-подобными объектными запросов
type: docs
weight: 60
url: /ru/java/work-with-xpath-like-object-queries/
description: Используя Aspose.3D for Java, вы можете выбрать один или несколько объектов в текущем узле, используя синтаксис запроса XPath-Like.
---
##  **Работа с XPath-подобными объектными запросов**
Используя Aspose.3D for Java, вы можете выбрать один или несколько объектов в текущем узле, используя синтаксис запроса XPath-Like. Синтаксис запроса был вдохновлен XPath, поэтому большинство концепций и синтаксиса похожи, синтаксис запроса совместим с URL, поэтому он будет использоваться в нашей облачной версии в будущем. Как правило, синтаксис состоит из**Условие имени префикса** / **Имя Состояние** /.

|**Префикс**|**Описание**|
| :- | :- |
| // |Глобальный селектор, любой потомок рассматривается как корневой узел для выполнения выбора|
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
